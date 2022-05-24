Nextcloud
=========

This is Ansible role that installs Nextcloud. Nextcloud is free and open-source self-hosted cloud storage. 

Requirements
------------

Ansible version >=2.1.0

Role Variables
--------------

Default variables you can view and in defaults/main.yml.

Usage
----------------

Add hosts where Nextcloud will be installed in your inventory file:
```
user@pc:~# vim /etc/ansible/hosts 
```

```
[storage]
192.168.1.10
```

Then clone and put this role in ~/.ansible/roles/

```
user@pc:~$ git clone https://github.com/emil9061/nextcloud.git 

user@pc:~$ mv nextcloud ~/.ansible/roles/
```

Then create and run the playbook: 

```
- hosts: storage
  roles:
    - nextcloud
```

```
user@pc:~$ ansible-playbook playbook.yml -u root -k
```

