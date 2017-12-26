ansible-mariadb
=========
[![Build Status](https://img.shields.io/travis/hispanico/ansible-mariadb.svg?style=flat-square)](https://travis-ci.org/hispanico/ansible-mariadb)
[![Galaxy](https://img.shields.io/badge/galaxy-hispanico.mariasb-blue.svg?style=flat-square)](https://galaxy.ansible.com/hispanico/mariadb/)

Install and configures Mariadb

Requirements
------------

This role requires Ansible 1.9 or higher.

Role Variables
--------------

Default values:

```yaml
mariadb_root_pw: Ch@ng3Me         # DB root password

databases:                        # List of Databases
  mydb:                           # DB name
    db_user_name: dbuser          # DB Username
    db_user_passwd: dbpasswd      # DB User password
    db_user_host: localhost       # DB User access from
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: all
  become: true
  remote_user: ansible

  roles:
    - ansible-mariadb

  vars:
    databases:                        
      db01:             
        db_user_name: db01user
        db_user_passwd: db01passwd
        db_user_host: localhost

      db02:             
        db_user_name: db02user
        db_user_passwd: db02passwd
        db_user_host: localhost     

```

License
-------

Licensed under the GPLv3 License. See the LICENSE file for details.

Author Information
------------------

Hispanico
