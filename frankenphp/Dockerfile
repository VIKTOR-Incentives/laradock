ARG PHP_VERSION=8.4
FROM dunglas/frankenphp:php${PHP_VERSION}-alpine

RUN install-php-extensions \
    pdo_mysql \
    mbstring \
    xml \
    gd \
    zip \
    intl \
    bcmath \
    exif \
    pcntl \
    opcache

ARG PUID=1000
ARG PGID=1000
RUN addgroup -g ${PGID} laradock && \
    adduser -D -G laradock -u ${PUID} laradock

WORKDIR /var/www
EXPOSE 8000
