# Voyager Admin Theme

![Voyager Frontend Screenshot](/readme-intro.jpg)

__The Missing Admin Theme for The Missing Laravel Admin.__

This [Laravel](https://laravel.com/) package adds frontend views, routes and assets to a [Voyager](https://laravelvoyager.com/) project.

It comes with a basic structure for frontend layouts (eg. header, footer, etc) and theme assets using the [Foundation](https://foundation.zurb.com) framework.

Built by [Hampus Ershagen](https://webient.se/).

---

## Prerequisites

- PHP >= 7.1.3
- Node & NPM
- Composer
- [Laravel Requirements](https://laravel.com/docs/installation)

---

## Installation

__1. Install Laravel + Voyager__
_(Replace the $VARs with your own values)_

```bash
# 1.0 Install Laravel
composer create-project --prefer-dist laravel/laravel $DIR_NAME

# 1.1 Require Voyager
cd $DIR_NAME && composer require tcg/voyager

# 1.2 Copy .env.example to .env and update the DB & App URL config
cp .env.example .env

# 1.3 Generate a Laravel key
php artisan key:generate

# 1.4 Run the Voyager Installer
php artisan voyager:install

# 1.5 Create a Voyager Admin User
php artisan voyager:admin $YOUR_EMAIL --create
```

__2. Install Voyager Admin Theme__

```bash
# 2.0 Require this Package in your fresh Laravel/Voyager project
composer require pvtl/voyager-frontend

# 2.1 Run the Installer
composer dump-autoload && php artisan voyager-frontend:install

# 2.3 Build the front-end theme assets
npm run dev

# 2.4 Set the Laravel search driver in your .env
echo "SCOUT_DRIVER=tntsearch" >> .env
```

_Any issues? See [the troubleshooting section](#toubleshooting) below._

---