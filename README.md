# dev_cakephp2

![56077045-8b3d8d80-5e12-11e9-8f04-6ea41ec2ba54](https://user-images.githubusercontent.com/5633085/56258537-d0abd480-610a-11e9-87ad-26186bc7d7b3.jpg)

tutorials

- CakePHP 2.10
- PHP7.2
- Nginx -v1.15.5
- Mysql 5.7

## dev

First, please refer to 1 if you are starting for the first time.  
Please refer to 2 if you use it after the second time.


- ① If you are starting for the first time

```
fork my repository
$ rm -rf cakephp2.10/cakephp2/cakephp/*
$ cd cakephp2.10/cakephp2/
$ vim cake2.10/cakephp2/cakephp/composer.json

{
    "name": "my_app",
    "require": {
        "cakephp/cakephp": "2.10.*"
    },
    "config": {
        "vendor-dir": "Vendor/"
    }
}

$ cd docker
$ docker-compose up -d
$ docker exec -it cake2-phpfpm sh
# cd /var/www/html/cakephp2
# php composer.phar install
# Vendor/bin/cake bake project /var/www/html/cakephp2
# composer create-project --prefer-dist cakephp/app cakephp
```
- change database

```
$ cd cakephp2.10/cakephp2/cakephp/Config
$ cp database.php.default database.php
$ vim database.php
host:mysql
database:my_app
login:root
pass:test
```

- ② One that starts from the second time
```
fork my repository
$ cd docker
$ docker-compose up -d
```

- accessl url

http://localhost:8080/

![スクリーンショット 2019-04-15 18 53 33](https://user-images.githubusercontent.com/5633085/56124577-ec4f9780-5fb1-11e9-91ac-f2ad050619a9.png)

