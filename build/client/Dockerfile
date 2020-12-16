FROM node:lts-alpine

WORKDIR /root/client/

COPY ./build/client/scripts/ /root/build/client/scripts/
RUN chmod +x /root/build/client/scripts/*

RUN apk update \
    && npm install -g npm \
    && npm install -g @vue/cli

ENTRYPOINT [ "/root/build/client/scripts/nomal_build.sh" ]