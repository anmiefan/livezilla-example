FROM php:7.2-apache

ENV livezilla_url https://www.livezilla.net/downloads/pubfiles/livezilla_server_7.1.0.9.zip

RUN apt-get update && \
    apt-get -y install wget && \
    docker-php-ext-install mysqli

COPY ./livezilla/ /
RUN chmod -R 777 /livezilla

COPY ./conf/apache2.conf /etc/apache2/
COPY ./conf/000-default.conf /etc/apache2/sites-available