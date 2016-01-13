# Development guide

## Install dependencies via composer

In the project folder run

    $ ./composer.phar install

to install dependencies.

If you add any dependencies in `composer.json` file, run 
    
    $ ./composer.phar update

to install new dependencies.

## Directory structure

- `app`: Application code
- `app/src`: All class files that follow the psr-4 autoloading standard (_see autoload in composer.json_)
- `app/templates`: Twig template files
- `config`: Configuration files (_\*.local.php are deployment specific files and ignored by git_)
- `data/cache/twig`: Twig's autogenerated cache files
- `data/log`: Log files
- `public`: Webserver Document root
- `test`: Unit test files
- `vendor`: Composer dependencies

## Special files

- `public\index.php`: Appliction entry point
- `config\{,*.}{global,local}.php`: Configuration files; \*.global.php are loaded first and then can be overriden by \*.local.php
- `app/dependencies.php`: Wiring dependencies
- `app/middleware.php`: Application middleware
- `app/routes.php`: All application routes

## Run it:

1. `$ cd gredu_labs`
2. `$ php -S 0.0.0.0:8888 -t public public/index.php`
3. Browse to http://localhost:8888