`dimmaryanto93.skywalking`
=========

Repository ini digunakan untuk menginstall [Apache Skywalking]() yaitu berfungsi Application Performance Monitoring atau APM untuk Linux

Support platform

- CentOS
- Oracle Linux 
- RedHat


Ansible - User Guide
------------

1. Authenticate with private-key for login ssh, generate ssh key on your local machine then use `ssh-copy-id user@your-ip-server` to copy public key to your server.


Requirements
------------

Untuk menggunakan role ini, kita membutuhkan package/collection 

- [ansible.posix](https://github.com/ansible-collections/ansible.posix)
- [community.general](https://github.com/ansible-collections/community.general)

Temen-temen bisa install, dengan cara 

```bash
ansible-galaxy collection install ansible.posix community.general
```

Atau temen-temen bisa menggunakan `requirement.yaml` file and install menggunakan `ansible-galaxy collection install -r requirement.yaml`, dengan format seperti berikut:

```yaml
---
collections:
  - community.general
  - ansible.posix
```

Role Variables
--------------

Ada beberapa variable yang temen-temen bisa gunakan untuk setting sonatype nexus-oss, diantaranya seperti berikut:

| Variable name                 | Example value       | Description |
| :---                          | :---                | :---        |


Dependencies
------------

Untuk mengginstall Sonatype Nexus OSS kita membuatuhkan Java Development Kit (JDK) sesuai dengan requirment dari official websiste [seperti berikut](https://help.sonatype.com/repomanager3/installation/system-requirements#SystemRequirements-Linux)

Kita bisa menggunakan role [oracle_java](https://galaxy.ansible.com/dimmaryanto93/oracle_java) atau install manualy


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```ansible
- hosts: servers
  become: true
  roles:
      - { role: dimmaryanto93.skywalking }
```

License
-------

MIT
