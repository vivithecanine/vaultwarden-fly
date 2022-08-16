# syntax=docker/dockerfile:1.4
# https://hub.docker.com/_/alpine/tags?page=1&name=3.16
FROM docker.io/alpine@sha256:1304f174557314a7ed9eddb4eab12fed12cb0cd9809e4c28f29af86979a3c870

RUN apk update && \
apk upgrade && \
apk add caddy && \
rm -rf /var/cache/apk/*

COPY Caddyfile /etc/caddy/Caddyfile

EXPOSE 8080/tcp

CMD ["caddy", "run", "--config", "/etc/caddy/Caddyfile", "--adapter", "caddyfile"]
