FROM phpdockerio/php73-fpm:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php-memcached php7.3-mysql php-redis php-xdebug php7.3-bcmath php7.3-bz2 php7.3-gd php7.3-gmp php-imagick php7.3-imap php-mongodb php7.3-odbc php7.3-phpdbg php7.3-soap php-ssh2 php7.3-xmlrpc php7.3-xsl php-yaml \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*