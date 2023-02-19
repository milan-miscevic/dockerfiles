FROM php:8.2-fpm

COPY --from=composer:2 /usr/bin/composer /usr/local/bin/composer

RUN apt-get update

RUN apt-get install unzip

RUN apt-get install -y libicu-dev && rm -rf /var/lib/apt/lists/*
RUN docker-php-ext-install intl

RUN pecl install xdebug
RUN docker-php-ext-enable xdebug
