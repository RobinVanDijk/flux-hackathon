FROM php:8.1-fpm

WORKDIR /app

COPY composer.json composer.lock ./

RUN apt-get update && apt-get install -y curl && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN composer install --no-dev --prefer-dist

COPY . .

EXPOSE 9000