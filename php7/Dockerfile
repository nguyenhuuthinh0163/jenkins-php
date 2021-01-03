FROM php:7.3.0-fpm
MAINTAINER thinh

RUN apt-get update -y && apt-get install -y default-mysql-client default-libmysqlclient-dev && \
    apt-get install -y libmcrypt-dev && \
    pecl channel-update pecl.php.net && \
    pecl install channel://pecl.php.net/mcrypt-1.0.2 && \
    docker-php-ext-install pdo_mysql && \
    docker-php-ext-enable mcrypt && \
    #zip,unzip
    apt-get install -y zip unzip && \
    #vim
    apt-get install -y vim curl

    #composer
RUN curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer && \
    chmod 777 /usr/local/bin/composer

RUN apt-get install 

RUN cd /var/www && \
    curl https://get.fuelphp.com/oil | sh

WORKDIR /var/www