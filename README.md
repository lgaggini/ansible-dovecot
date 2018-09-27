# ansible-getmail

ansible-dovecot is an Ansible role to install and configure dovecot on a debian based OS.

It performs: 

* installation of dovecot package(s)
* creation of dedicated user and group for dovecot vmail
* creation of dedicated folder for dovecot vusers home
* configuration of ssl
* configuration of mail location and type
* configuration of basic auth passwd file and userdb static
* configuration of user accounts
* enable saslauth

## Install
### Clone
```bash
git clone https://github.com/lgaggini/ansible-dovecot.git
```
## Configuration

The configuration is done by vars listed and explained in [defaults/main.yml](https://github.com/lgaggini/ansible-dovecot/blob/master/defaults/main.yml) file.

## Usage

```
- name: bootstrap an ubuntu cloud image for dovecot
  hosts: imapserver
  vars_files:
    - group_vars/dovecot.yml

  roles:
    - { role: dovecot, tags: ['dovecot'] }
```
