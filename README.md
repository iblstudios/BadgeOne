IBL OpenBadges Server (BadgeOne.com)
====================================

This is the IBLOpenBadges Server platform. A platform to award your own institution's badges. 
The badges you create and earn with this server are compatible with the specifications of the OpenBadges project.

This package was developed by [IBL Studios](http://iblstudios.com/).

## OpenBadges specifications
* [Mozilla OpenBadges] (http://openbadges.org/)
* [Mozilla OpenBadges wiki] (https://github.com/mozilla/openbadges-backpack/wiki/)
* [Mozilla OpenBadges latest specs] (https://openbadgespec.org/)

###Requirements:
* PHP > 5.3.9 (php5-mysql, php5-json) (Recommended > php 5.4.0)
* MySQL 5.x (PDO connections are used with php5)
* Apache2.4 server (you could use Nginx; remember to configure the options properly)
* mod_rewrite (to protect certain directories with .htaccess files)
* Certain directories require write permissions (defined in installation process)

###Prepare Installation:
* Create your database and user, and grant privileges.
* Load the main database. The SQLdump file is provided under `sql/iblstudiosbadges.model.sql.dump`.
* Configure your VirtualHost (absolute domain or subdomain). Sample: `virtualhost/apache-2.4-sample.conf`.
* The server, API and OAuth platform files are given under the `www/` directory. Place the contents
  in the path you have defined for your VirtualHost.

###Install and configure the Badges Server:
* Before releasing your server to the public, you will need to correctly configure your database connection
  and your institution's data.
* Request this page with a browser: `http://_your_badges_server_uri_/install.php`.
* Follow step-by-step instructions defined on `install.php`. The installation page will guide you 
  to perfom the changes on the configuration's parameters and set directory permissions correctly.
* The last step allows you to create the `admin` user. Remember to change the default password when you
  access for the first time (default password: `admin123`).
* Important! Remove the `install.php` file when you finish your installation.

###About OAuth2
* This platform uses OAuth2.0 authentication.
   [OAuth 2.0] (http://oauth.net/2/)
   [OAuth 2.0 Server PHP] (http://bshaffer.github.io/oauth2-server-php-docs/)