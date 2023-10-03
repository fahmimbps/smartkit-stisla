# SMARTKIT STISLA THEME

## Apa itu?

SMARTKIT adalah Aplikasi Sistem Monitoring Administrasi, Teknis dan Kinerja 
Individu Terpadu [BPS Provinsi Jawa Barat](https://jabar.bps.go.id).

## Teknologi

Framework PHP : CodeIgniter 4

Theme : stisla

Database : sqlite3

Repositori untuk backend : https://github.com/fahmimbps/smartkit-ci/

Repositori untuk theme stisla : https://github.com/fahmimbps/smartkit-stisla/

## Instalasi & update

1. git clone https://github.com/fahmimbps/smartkit-ci.git smartkit
2. cd smartkit/public/template
3. git clone https://github.com/fahmimbps/smartkit-stisla.git .
4. yarn
5. cd ..
6. Copy `env` to `.env` and tailor for your app, specifically the baseURL
   and any database settings
8. php spark serve
   
## Server Requirements

PHP version 7.4 or higher is required, with the following extensions installed:

- [intl](http://php.net/manual/en/intl.requirements.php)
- [mbstring](http://php.net/manual/en/mbstring.installation.php)

Additionally, make sure that the following extensions are enabled in your PHP:

- json (enabled by default - don't turn it off)
- [mysqlnd](http://php.net/manual/en/mysqlnd.install.php) if you plan to use MySQL
- [libcurl](http://php.net/manual/en/curl.requirements.php) if you plan to use the HTTP\CURLRequest library
  
## Important Change with index.php

`index.php` is no longer in the root of the project! It has been moved inside the *public* folder,
for better security and separation of components.

This means that you should configure your web server to "point" to your project's *public* folder, and
not to the project root. A better practice would be to configure a virtual host to point there. A poor practice would be to point your web server to the project root and expect to enter *public/...*, as the rest of your logic and the
framework are exposed.

**Please** read the user guide for a better explanation of how CI4 works!

## Repository Management

We use GitHub issues, in our main repository, to track **BUGS** and to track approved **DEVELOPMENT** work packages.
We use our [forum](http://forum.codeigniter.com) to provide SUPPORT and to discuss
FEATURE REQUESTS.

This repository is a "distribution" one, built by our release preparation script.
Problems with it can be raised on our forum, or as issues in the main repository.
