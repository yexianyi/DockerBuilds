# This is a comment
FROM ubuntu:16.04

MAINTAINER Xianyi Ye <yexianyi@sohu.com>

RUN sed -i 's/archive.ubuntu.com/hk.archive.ubuntu.com/g' /etc/apt/sources.list \
	&& apt-get update \
	&& apt-get install -y python-software-properties software-properties-common \
	&& add-apt-repository ppa:webupd8team/java \
    	&& apt-get update  \
	&& echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections \
	&& apt-get install -y oracle-java8-installer oracle-java8-set-default \
	&& apt-get clean \