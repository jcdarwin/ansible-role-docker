mebooks.ansible-role-docker
===========================

Ansible role for installing Docker on Ubuntu and Centos distributions, based on [rgarrigue.docker](https://github.com/rgarrigue/ansible-role-docker).

Install [Docker](https:/docker.com) as of 2017, i.e. `docker-ce` as in community edition, and remove the deprecated packages `docker-engine`, `docker` etc [![Build Status](https://travis-ci.org/rgarrigue/ansible-role-docker.svg?branch=master)](https://travis-ci.org/rgarrigue/ansible-role-docker)

Requirements
------------

Developped and tested on *Ubuntu Server 16.10 Yakkety*, and *CentOS 7*

Role Variables
--------------

The only one likely to be overriden is `user`, which default to `docker` but you might want to set to your own daily user

- apt_key_signature
- apt_key_url
- apt_repository
- yum_baseurl
- yum_gpgkey
- user
- deprecated_packages

Dependencies
------------

None

Example Playbook
----------------

    - hosts: mydockercloud
      vars:
        - user: me.myself

      roles:
        - role: mebooks.ansible-role-docker

License
-------

GPLv3

Author Information
------------------

Jason Darwin
