# docker-apache-php

Configured to also parse HTML files through PHP.

## Volumes

> Adjust volumes before building to customize.

| Source | Target |
| ------ | ------ |
| ./www  | /var/www |
| ./conf/.env  | /etc/environment |
| ./conf/vhosts | /etc/apache2/sites-enabled |
| ./logs/httpd | /var/log/apache2 |
| ./conf/php/www.ini | /usr/local/etc/php/conf.d/www.ini |

## Default Virtual Host

> Adjust default or use it as a reference for new virtual hosts.
> Can be adjusted post-build. Server restart required.

| Host | Document Root | Config |
| ---- | ------------- | ------ |
| localhost:8080 | /var/www/html | ./conf/vhosts/site.conf |

## Build

```console
docker-compose up --build
```
