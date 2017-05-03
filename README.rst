ansible-tftp
=============

.. image:: http://img.shields.io/badge/ansible--galaxy-tftp-blue.svg
  :target: https://galaxy.ansible.com/narfman0/tftp/

.. image:: https://travis-ci.org/narfman0/ansible-tftp.png?branch=master
    :target: https://travis-ci.org/narfman0/ansible-tftp

Ansible module for tftp

Usage
-----


A vagrant file has been included for easier testing. To use::

    vagrant up --provider virtualbox

This will provision the machine such that a working tftp
is ready to run.

Running playbook directly
~~~~~~~~~~~~~~~~~~~~~~~~~

I have a tftp host defined in `/etc/ansible/hosts`::

    [tftp]
    tftp1

Assuming you have hosts identified (overriding playbook vars
or globally in `/etc/ansible/hosts`), you may invoke the
playbook directly with::

    ansible-playbook playbook.yml -v

Example
-------

Playbook::

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
      - { role: narfman0.tftp }

License
-------

Please see included LICENSE file for license specifics

Copyright 2017 Jon Robison
