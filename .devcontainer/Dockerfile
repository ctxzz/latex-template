# ctxzz/latex-template
# https://hub.docker.com/r/ctxzz/latex-template/

FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    xdvik-ja \ 
    evince \
    texlive-full \
    latexmk \
    language-pack-ja \
    wget \
    xzdec \
    git \
    cpanminus \
    make \
    perl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN tlmgr init-usertree
RUN kanji-config-updmap-sys ipaex

WORKDIR /workdir

VOLUME ["/workdir"]

CMD ["bash"]

