artifactory
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-artifactory.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-artifactory)

Provides artifactory for your system.


Example Playbook
----------------

This example is taken from `molecule/default/playbook.yml`:
```
---
- name: Converge
  hosts: all
  gather_facts: false
  become: true

  roles:
    - robertdebock.bootstrap
    - robertdebock.java
    - robertdebock.artifactory

```

Role Variables
--------------

These variables are set in `defaults/main.yml`:
```
---
# defaults file for artifactory

# The version of Artifactory to install
artifactory_version: 6.5.2

# The location where Artifactory should install.
artifactory_download_directory: /opt

```

Requirements
------------

- Access to a repository containing packages, likely on the internet.
- A recent version of Ansible. (Tests run on the last 3 release of Ansible.)

The following roles can be installed to ensure all requirements are met, using `ansible-galaxy install -r requirements.yml`:

---
- robertdebock.bootstrap
- robertdebock.java


Context
-------

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/drawings/artifacts/artifactory.png "Dependency")


Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.4|ansible 2.5|ansible 2.6|ansible 2.7|ansible devel|
|------------|-----------|-----------|-----------|-----------|-------------|
|alpine-edge*|yes|yes|yes|yes|yes*|
|alpine-latest|yes|yes|yes|yes|yes*|
|archlinux|yes|yes|yes|yes|yes*|
|centos-6|yes|yes|yes|yes|yes*|
|centos-latest|yes|yes|yes|yes|yes*|
|debian-latest|yes|yes|yes|yes|yes*|
|debian-stable|yes|yes|yes|yes|yes*|
|debian-unstable*|yes|yes|yes|yes|yes*|
|fedora-latest|yes|yes|yes|yes|yes*|
|fedora-rawhide*|yes|yes|yes|yes|yes*|
|opensuse-leap|yes|yes|yes|yes|yes*|
|opensuse-tumbleweed|yes|yes|yes|yes|yes*|
|ubuntu-artful|yes|yes|yes|yes|yes*|
|ubuntu-devel*|yes|yes|yes|yes|yes*|
|ubuntu-latest|yes|yes|yes|yes|yes*|

A single star means the build may fail, it's marked as an experimental build.

Testing
-------

[Unit tests](https://travis-ci.org/robertdebock/ansible-role-artifactory) are done on every commit and periodically.

If you find issues, please register them in [GitHub](https://github.com/robertdebock/ansible-role-artifactory/issues)

To test this role locally please use [Molecule](https://github.com/metacloud/molecule):
```
pip install molecule
molecule test
```
There are many specific scenarios available, please have a look in the `molecule/` directory.


License
-------

Apache-2.0


Author Information
------------------

[Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
