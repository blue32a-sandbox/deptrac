FROM php:8.2-cli

RUN apt-get update \
    && apt-get install -y \
        git \
        zip \
        unzip \
        graphviz \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

COPY --from=composer:2.5 /usr/bin/composer /usr/bin/composer

COPY php.ini /usr/local/etc/php
