FROM php:8.1-fpm-alpine

# PHP Extensions
RUN docker-php-ext-install pdo pdo_mysql sockets

RUN curl -sS https://getcomposer.org/installer​ | php -- \
    --install-dir=/usr/local/bin --filename=composer

RUN chown -R www-data:www-data /var/www/html \
    && chmod  775 -R /var/www/html

EXPOSE 80
CMD php -S 0.0.0.0:80 -t public
