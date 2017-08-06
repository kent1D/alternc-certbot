# Purpose

It's a alternc plugin to help to manage certbot certificates.

It's enable and generate a certbot certificat to panel alternc.

# Requirement

You need :
* debian server (wheezy or jessie)
* alternc >= 3.2
* certbot package
 * with wheezy : [from antonbatenev backport](https://software.opensuse.org//download.html?project=home%3Aantonbatenev%3Aletsencrypt&package=certbot)
 * with jessie : [from backport](https://packages.debian.org/jessie-backports/certbot)


# Installation

You can download last package from [release page](../../releases/latest)

```shell
cd ~
wget https://github.com/AlternC/alternc-certbot/releases/download/0.0.2/alternc-certbot_0.0.2-_all.deb
dpkg -i alternc-certbot_0.0.2-_all.deb
apt-get -f install
```

# Packaging from source

To generate package we use [fpm tool](https://github.com/jordansissel/fpm)

```shell
apt-get install ruby ruby-dev rubygems build-essential
gem install --no-ri --no-rdoc fpm

git clone https://github.com/AlternC/alternc-certbot
cd alternc-certbot
make 

```


# ROADMAP

* [x] Auto renew panel certificat (0.0.2)
* [ ] Auto detect new domain add from panel
* [ ] Auto renew all domains 