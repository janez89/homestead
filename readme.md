# Laravel Homestead

The official Laravel local development environment.

Official documentation [is located here](http://laravel.com/docs/homestead?version=4.2).


# Changes

## installed softwares

* Nginx
* PHP 5.5
* MySQL
* Memcached
* Redis
* Beanstalkd
* Nodejs (grunt, gulp, bower)


MySQL access: root, vagrant

## Install

Add Vagrant box: `vagrant box add laravel/homestead`

Clone repository: `git clone https://github.com/janez89/homestead.git Homestead`

Generate SSH key for login and edit `Homestead.yaml`

`ssh-keygen -t rsa -C "you@homestead"`

Configure Your Shared Folders in `Homestead.yaml`

Configure Your Nginx Sites in `Homestead.yaml`

Add domain to hosts file.
 On Mac and Linux, this file is located at `/etc/hosts`. On Windows, it is located at `C:\Windows\System32\drivers\etc\hosts`. The lines you add to this file will look like the following:

`192.168.10.10  homestead.app`

Adding Additional Sites after added `Homestead.yaml` run `vagrant provision`.

# Ports

* SSH: 2222 -> Forwards To 22
* HTTP: 8000 -> Forwards To 80
* HTTP: 9000 -> Forwards To 9000  (Grunt server for Angular JS)
* MySQL: 33060 -> Forwards To 3306
