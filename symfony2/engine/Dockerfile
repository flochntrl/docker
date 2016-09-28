FROM php:5.6-fpm

RUN apt-get update \
    && apt-get install -y \
        apt-utils \
        libicu-dev \
        zlib1g-dev \
        libmcrypt-dev \
    && docker-php-ext-install \
        intl \
        mbstring \
        pdo_mysql \
        mcrypt \
    && php -r "readfile('https://getcomposer.org/installer');" | php -- --install-dir=/usr/local/bin --filename=composer \
    && chmod +x /usr/local/bin/composer

RUN usermod -u 1000 www-data
