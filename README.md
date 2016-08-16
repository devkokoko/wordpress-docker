## Development

### WordPress plugin

Requirements:
- docker (native, no boot2docker)
- docker-compose

Launch the WordPress development environment.

**Be sure you have nothing running on port 80, and also that you are using the native version of Docker.**

```
$ dev/restart.sh
```

If everything went OK, you should be able to access the WordPress instance on `http://localhost` and the admin panel on `http://localhost/wp-admin/`.

If you get a lot of errors like the following, simply restart docker:
```
Warning: copy(/var/www/html//wp-content/themes/twentyfourteen/category.php): failed to open stream: No such file or directory in phar:///bin/wp/php/commands/core.php on line 220
```

Admin user credentials:
- login: admin
- password: admin


In the admin panel, you can now go to `plugins` and enable the `Algolia Search` plugin.

Note that the whole WordPress dir is mounted as a volume so that you can edit anything on the fly in `./wordpress`.
