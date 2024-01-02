# Ansible role [alternatives](https://galaxy.ansible.com/ui/standalone/roles/buluma/alternatives/documentation)

Set alternatives

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-alternatives/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-alternatives/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-alternatives.svg)](https://github.com/buluma/ansible-role-alternatives/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-alternatives.svg)](https://github.com/buluma/ansible-role-alternatives/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-alternatives.svg)](https://github.com/buluma/ansible-role-alternatives/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/alternatives)](https://galaxy.ansible.com/ui/standalone/roles/buluma/alternatives/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-alternatives/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: buluma.alternatives
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-alternatives/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: prepare
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: buluma.bootstrap

  tasks:
    - name: make a fake binary
      ansible.builtin.file:
        path: /bin/my_fake_binary
        state: touch
        mode: "0755"
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-alternatives/blob/master/defaults/main.yml):

```yaml
---
# defaults file for alternatives

# This is an example of how to use python3.7 on a system that has both
# python 2.7 and python 3.7.
# alternatives_list:
#   - name: python
#     link: /usr/bin/python2.7
#     path: /usr/bin/python
#   - name: python
#     link: /usr/bin/python3.7
#     path: /usr/bin/python

alternatives_list: []
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-alternatives/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-alternatives/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Alpine](https://hub.docker.com/repository/docker/buluma/alpine/general)|all|
|[Amazon](https://hub.docker.com/repository/docker/buluma/amazonlinux/general)|Candidate|
|[EL](https://hub.docker.com/repository/docker/buluma/enterpriselinux/general)|8|
|[Debian](https://hub.docker.com/repository/docker/buluma/debian/general)|all|
|[Fedora](https://hub.docker.com/repository/docker/buluma/fedora/general)|all|
|[opensuse](https://hub.docker.com/repository/docker/buluma/opensuse/general)|all|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-alternatives/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-alternatives/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-alternatives/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)

