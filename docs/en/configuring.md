Configuring PHP Censor
======================

The PHP Censor configuration on the server is automatically generated into the `config.yml` file during installation.
One might need to also edit the file manually.

For example, one could log into PHP Censor and go into the settings to disable it. But if you have already set up a
username/password pair and have forgotten the password, and if the server is on a local network, and it's not sending
the `forgot password` email, then editing the config file manually would be handy. To do so, just edit the `php-censor`
section in the config file (which is in [yaml format](https://en.wikipedia.org/wiki/YAML)), and add

```yml
php-censor:
  security:
    disable_auth:    true
    default_user_id: 1
```

where you can get the `default_user_id` by logging into the database and selecting your user ID from the `users` table in
the PHP Censor database.
