
FROM ubuntu:latest

RUN apt-get update
RUN apt-get -y install locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
    
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
ENV TERM xterm

#ssh接続用のライブラリをインストール
RUN apt-get install -y openssh-server

COPY . root/sh

#shell scriptを起動
ENTRYPOINT ["root/sh/init.sh"]
