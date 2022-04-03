FROM ubuntu:20.04

EXPOSE 2222

ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update

# Nano
RUN apt-get install -y nano

# Sudo
RUN apt-get install -y sudo

# SSH
RUN apt-get install -y openssh-server
RUN passwd & echo 12345678 & echo 12345678
RUN service ssh start

# Git
RUN apt install -y git

# NodeJS
RUN apt install -y build-essential checkinstall
RUN apt install -y libssl-dev
RUN apt install -y nodejs
RUN apt install -y npm