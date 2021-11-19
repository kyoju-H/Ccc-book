FROM node:12.18.3-alpine

ARG WORKDIR
ARG CONTAINER_PORT

ENV HOME=/${WORKDIR} \
    LANG=C.UTF-8 \
    TZ=Asia/Tokyo \
    HOST=0.0.0.0

WORKDIR ${HOME}

RUN apk update && \
    apk upgrade && \
    apk add --no-cache \
        libtool \
        automake \
        autoconf \
        g++ \
        libc6-compat \
        libjpeg-turbo-dev \
        libpng-dev \
        make \
        nasm && \
    yarn install &&\
    rm -rf /var/cache/apk/*

EXPOSE ${CONTAINER_PORT}