# Notes on Installing WordPress on a Raspberry Pi 

Notes from 2019-12-16.

## Instructions
https://projects.raspberrypi.org/en/projects/lamp-web-server-with-wordpress


## Update Things
````bash
sudo apt-get update && sudo apt-get dist-upgrade
````

## Install Apache
````bash
sudo apt-get install apache2 -y
````

## Initial PHP
````bash
sudo apt-get install php -y
````

## Install MySQL/MariaDB
See https://projects.raspberrypi.org/en/projects/lamp-web-server-with-wordpress/7

## Restart Apache
````bash
sudo service apache2 restart
````

## Install WordPress
````bash
cd /var/www/html
sudo rm -rf *
sudo service apache2 restart
sudo wget http://wordpress.org/latest.tar.gz
sudo tar xzf latest.tar.gz
sudo mv wordpress/* .
sudo rm -rf wordpress latest.tar.gz
sudo chown -R www-data: .
````

