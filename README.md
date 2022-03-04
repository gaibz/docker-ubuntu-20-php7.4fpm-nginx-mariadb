# Dockerize Ubuntu + Nginx + PHP7.4 FPM

This is just a base image for a project that require 

- Ubuntu 
- php7.4-fpm
- nginx
- mysql

Personally for my own use case 

Github Repo : https://github.com/gaibz/docker-ubuntu-20-php7.4fpm-nginx-mariadb

Docker Repo : https://hub.docker.com/repository/docker/gaibz/ubuntu20-php7.4-nginx-mariadb

# Setup & Build 

## Tag
```
gaibz/docker-ubuntu-20-php7.4fpm-nginx-mariadb:latest
```

## Nginx Server Config File

```
/etc/nginx/sites-enabled/*
```


## PHP Version : 7.4 (with default ubuntu repo) Config File

default php-fpm is listen on 127.0.0.1:9000

fpm pool
```
/etc/php/7.4/fpm/pool.d/www.conf
```
fpm ini
```
/etc/php/7.4/fpm/php.ini
```

## MariaDB / MySQL Config File

there is so much reason why I prefer Mariadb over Mysql. So let me be my self;

```
/etc/mariadb.conf.d/50-server.cnf
```

## app directory

```
/var/www/app
```

## Exposed Port

```
80/tcp (Nginx)
3306/tcp (MariaDB/MySQl)
```
