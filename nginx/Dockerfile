FROM nginx:stable-alpine

ARG UID
ARG GID

COPY nginx.conf /etc/nginx

RUN addgroup -g ${GID} --system pocidock
RUN adduser -G pocidock --system -D -s /bin/sh -u ${UID} pocidock
# RUN sed -i "s/user  nginx/user pocidock/g" /etc/nginx/nginx.conf

RUN rm /etc/nginx/conf.d/default.conf

RUN mkdir -p /var/www