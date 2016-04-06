Ansible role: Docker Registry
==========================

Installs a Docker registry


The role uses the following [Ansible tags](http://docs.ansible.com/ansible/playbooks_tags.html) to control the provisioning process:

* ``install`` - installs Docker Registry node software
* ``configure`` - sets up Docker Registry node at master, and configure Systemd if needed.
* ``deploy`` - enable and start a Systemd unit if a VM or physical machine is being used or in the case of Docker, add a Supervisor config
* ``test`` - check the application's HTTP endpoint for a response to confirm it is working and check if Docker Registry is working pulling the list of plugins using Docker Registry-cli.

Requirements
------------

* [Ansible facts](https://github.com/idi-ops/ansible-facts)
* The certificates and keys used to provide TLS support are only for testing
  propose. DO NOT USE THEM AT PRODUCTION.

Role Variables
--------------

Please refer to the [defaults/main.yml](defaults/main.yml) file for a list of variables along with additional documentation.

Example Playbook
----------------

```
---

- hosts: registry
  become: true

  roles:
    - ansible-facts
    - ansible-docker-registry
 
```
License
-------

MIT

Author Information
------------------

* Inclusive Design Research Centre (OCAD University)
* Raising the floor - International

