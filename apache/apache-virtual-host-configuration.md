### Apache Virtual Host Configuration

**Description: **

> Config virtual host to redirect different request source \(ip-base, domain-name base \) to relevant destination
>
> Specs:
> * Apache 2.4
> * Ubuntu 16.04
> * Php 5.6

**Config:**

```
# vi /usr/local/apache2/sites-available/vhosts.conf
NameVirtualHost *:80

<VirtualHost *:80>
    ServerAdmin admin@webmaster.com

    DocumentRoot "/var/www/ex1"
    ServerName example_1.com
    ServerAlias www.example_1.com

    ErrorLog "/var/log/apache2/example_1_error_log"
    CustomLog "/var/log/apache2/example_1_access_log" common
</VirtualHost>

<VirtualHost *:80>
   DocumentRoot "/var/www/ex2"
    ServerName example_2.com
    ServerAlias www.example_2.com

    ErrorLog "/var/log/apache2/example_2_error_log"
    CustomLog "/var/log/apache2/example_2_access_log" common
</VirtualHost>
```

**Source: **

* [https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-14-04-lts](https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-14-04-lts)

**Extra infomation:**

TO\_BE\_UPDATE

**Tags:**

\#apache \#virtualhost \#apache\_directory

##### 



