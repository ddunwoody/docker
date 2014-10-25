FROM ubuntu:14.04
MAINTAINER David Dunwoody <david.dunwoody@gmail.com>
RUN apt-get update && apt-get install -y ant build-essential git openjdk-7-jdk
WORKDIR /tmp
RUN git clone git://github.com/cryptobiu/scapi.git
WORKDIR /tmp/scapi
RUN git submodule init && git submodule update
RUN make && make install prefix=/usr
