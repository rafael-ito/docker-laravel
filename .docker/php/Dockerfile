FROM php:7.3-fpm

RUN apt-get update \
    && apt-get install -y \
        apt-utils \
        build-essential \
        libfreetype6-dev \
        libmcrypt-dev \
        libjpeg-dev \
        libicu-dev \
        libpng-dev \
        libzip-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install \
    pdo_mysql \
    gd \
    mbstring \
    mysqli \
    zip

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
