# Ansible Role: phpMyAdmin

An Ansible role that installs phpMyAdmin on Ubuntu.

If nginx is installed phpMyAdmin will be configured for it in `/etc/nginx/global.d/phpmyadmin.conf`. The files in that
directory should be included in all virtual hosts with `include /etc/nginx/global.d/*.conf;`.

## Requirements

For phpMyAdmin to work a web server (e.g. nginx), php and MySQL have to be installed.

## Role Variables

Available variables are listed below, along with default values:

    phpmyadmin_php_fpm_socket: php-fpm

    phpmyadmin_server_host: localhost
    phpmyadmin_server_auth_type: config
    phpmyadmin_server_user: root
    phpmyadmin_server_password: root

    phpmyadmin_custom_template_filename: config.php.j2

## Dependencies

None

## Example Playbook

    - hosts: all
      roles:
        - { role: mjanser.phpmyadmin }

## License

MIT
