# ansible-role.mysql_percona

Install
========
```
git submodule add git@github.com:Waldz/ansible-role.mysql_percona.git roles/mysql_percona
```

Example
========
```
- name: Basic configuration to all servers
  hosts: all
  sudo: true
  roles:
    - role: mysql_percona
  vars:
    - mysql_databases:
      - name: test
    - mysql_users:
      - user: root
        password: suPERpass
        priv: "*.*:ALL,GRANT"
        host: "%"
```
