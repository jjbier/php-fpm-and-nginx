FROM php:7.1.30-fpm

LABEL maintainer="Xabier Fernández <jjbier@gmail.com>"

RUN yes | pecl install xdebug \
    && docker-php-ext-enable xdebug

# here I'm copying the config file we will discuss in the next section
COPY ./xdebug.ini /usr/local/etc/php/conf.d/

ENV PS1="\u@\h:\w\\$ "
 
CMD ["php-fpm"]