FROM ubuntu:20.04

RUN apt-get update
RUN apt-get -y install openjdk-17-jdk-headless
RUN apt-get -y install mercurial git
RUN hg clone http://hg.openjdk.java.net/code-tools/asmtools/
RUN apt-get -y install less vim
RUN apt-get -y install ant
RUN cd asmtools/build ; JDK_JAVAC_OPTIONS="-encoding UTF-8" ant jar
RUN cp asmtools-7.0-build/binaries/lib/asmtools.jar /
RUN apt-get -y install autoconf make zip unzip
RUN apt-get -y install build-essential
RUN apt-get -y install libx11-dev libxext-dev libxrender-dev libxrandr-dev libxtst-dev libxt-dev
RUN apt-get -y install libcups2-dev
RUN apt-get -y install libfontconfig1-dev
RUN apt-get -y install libasound2-dev

CMD ["/bin/bash"]

