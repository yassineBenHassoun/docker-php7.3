# Docker-compose-php73-apache

Image Docker compose PHP 7.3-apache-stretch with Mysql mariadb

### Requirements
---

- Apache 2.4
- PHP 7.3-apache-stretch
- MySQL 5.7
- Composer

### Struct Folder
---

# Dockerfile config
- ./docker/images/application/Dockerfile

# All config Apache - Mysql - Php
  - ./docker/conf/apache/virtualhost.conf:/etc/apache2/sites-enabled/000-default.conf:ro
- ./docker/conf/php/php.ini:/usr/local/etc/php/php.ini
- ./docker/conf/php/php-cli.ini:/usr/local/etc/php/php-cli.ini
- ./ourapp/application:/var/www/html
      

# Source project
- ./ourapp/application/public:/var/www/html

### Image Docker
---
- mysql
- phpmyadmin
- apache

### Installation
---

```
# Run container docker
sudo docker-compose up -d 

# Execute container redis-cli with docker
sudo docker-compose exec redis redis-cli
```