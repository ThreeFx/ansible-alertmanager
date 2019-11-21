alertmanager
=========

Ansible role to set up Alertmanager

Requirements
------------

A running prometheus instance, e.g. created with [my
role](https://github.com/ThreeFx/ansible-prometheus).

Role Variables
--------------

| Variable Name | Default Value | Description |
--------------- |---------------|--------------

Dependencies
------------

None.

Example Playbook
----------------

    hosts: myhosts
    roles:
      - role: alertmanager
        vars:
          alertmanager_receivers:
            - name: 'mywebhook'
              webhook_configs:
                - send_resolved: true
                  url: 'http://somehost:someport'

License
-------

BSD

Author Information
------------------

Find me on [GitHub](https://github.com/ThreeFx).
