keycloak
=========
[![Build Status](https://travis-ci.org/andrewrothstein/ansible-keycloak.svg?branch=master)](https://travis-ci.org/andrewrothstein/ansible-keycloak)

Installs [KeyCloak](http://www.keycloak.org/)

Requirements
------------

See [meta/main.yml](meta/main.yml)

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------

```yml
- hosts: servers
  roles:
    - keycloak
  vars:
    keycloak_admin_password: "test123"
    keycloak_postgresql_password: "pass123"
    keycloak_postgresql_host: "localhost"
    keycloak_postgresql_database: "keycloak"
    keycloak_postgresql_connection_url: "jdbc:postgresql://{{ keycloak_postgresql_host }}:5432/{{ keycloak_postgresql_database }}"
    keycloak_http_port: 8080
    keycloak_https_port: 8443
    keycloak_nginx_max_filesize: "50M"
    keycloak_site_name: "{{ ansible_default_ipv4.address }}"
    keycloak_certbot_mail_address: "test@test.com"
```

License
-------

MIT

Authors
--------

* [Rodgers Andati ](https://github.com/andati)
* Andrew Rothstein <andrew.rothstein@gmail.com>