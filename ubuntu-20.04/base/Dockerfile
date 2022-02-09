FROM ubuntu:20.04

LABEL maintainer="Cristian Mello <cristianc.mello@gmail.com>"


ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update \
    && apt-get install -y \
        apt-utils

RUN apt-get install -y \
        locales \
    && dpkg-reconfigure locales

RUN locale-gen en_US.UTF-8

ENV LANGUAGE=en_US.UTF-8
ENV LC_ALL=en_US.UTF-8
ENV LC_CTYPE=en_US.UTF-8
ENV LANG=en_US.UTF-8
ENV TERM xterm


RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && \
    rm /var/log/lastlog /var/log/faillog