FROM php:7.2-fpm

ARG XDEBUG
COPY ./provision.sh /

RUN bash /provision.sh

COPY ./docker-entrypoint.sh /
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["php-fpm", "-F", "-R"]

EXPOSE 9000