# Docker-based Drupal stack

This is a modified version of [Docker4Drupal from Wodby](https://github.com/wodby/docker4drupal) 

Steps to get it up and running:
--------------------
```
$ docker-compose up -d
$ docker-compose exec php composer install
$ docker-compose exec php drush cr
```

Sequel Pro:
--------------------
localhost: 127.0.0.1<br>
user: drupal<br>
password: drupal<br>
database: drupal<br>
port: 3306

Database dump:
--------------------
```
$ doc exec mariadb sh -c 'exec mysqldump -uroot -ppassword drupal' > dump/drupal.sql
```
