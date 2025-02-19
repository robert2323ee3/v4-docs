# ⚙️ Configuring

Chevereto V4 uses [environment variables](environment.md) for configuring system level settings.

💡 Environment variables configured at `ENV` system level will **override** the configuration at `app/env.php`.

## Using `app/env.php`

For the most common use-case, set the system settings at the [app/env.php](env.php.md) file.

## Using `ENV`

This applies where system environment variables can be configured. In this case, variables are handled in a plain text format like in the example below:

```plain
CHEVERETO_DB_HOST=localhost
```

### Apache HTTP Web Server (PHP module)

If PHP is provided using `mpm_prefork` you must refer to the documentation on [Apache HTTP Server environment variables](https://httpd.apache.org/docs/current/env.html).

### Other setups

For these you will be running [PHP-FPM](https://www.php.net/manual/en/install.fpm.configuration.php) so you can add those settings at your `php-fpm.conf` file.

### Application servers

For these you will be running PHP CLI so you should be able to pass those at `php.ini` for your CLI. You can also `export` those in your shell.

👉 Refer to the documentation of each application server for the best way to pass environment variables to Chevereto.

### Container

Pass the environment variables to the container run command or at `docker compose` layer.
