# Hybrid\\Support

Hybrid Support is an add-on package for the [Hybrid Core](https://github.com/justintadlock/hybrid-core) WordPress framework.
This package provides necessary support classes, tools.

## Requirements

* WordPress 4.9+.
* PHP 5.6+ (preferably 7+).
* [Composer](https://getcomposer.org/) for managing PHP dependencies.

## Documentation

This project is only meant to work in conjunction with the Hybrid Core framework.  If you're not already working with and building a theme using it, the following will be useless.

### Installation

First, you'll need to open your command line tool and change directories to your theme folder.

```bash
cd path/to/wp-content/themes/<your-theme-name>
```

Then, use Composer to install the package.

```bash
composer require justintadlock/hybrid-support
```

### Register the service provider

You need to register the service provider during your bootstrapping process.  In your bootstrapping code, you should have something like the following:

```php
$app = new \Hybrid\Core\Application();
```

After that point, you can register the service provider:

```php
Use \Hybrid\Support\Contracts\Bootable;
Use \Hybrid\Support\Contracts\Displayable;
Use \Hybrid\Support\Contracts\Renderable;

class SomeClass extends Renderable, Displayable implements Bootable {

}
```

## Copyright and License

This project is licensed under the [GNU GPL](http://www.gnu.org/licenses/old-licenses/gpl-2.0.html), version 2 or later.

2021 &copy; [Justin Tadlock](http://justintadlock.com).
