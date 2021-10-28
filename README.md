SSHD Trusted User Setup
=========

This role can be used to set up OpenSSH's `sshd_config` to allow user
authentication based on certificates signed by a trusted Root CA key.

[![Build Status](https://github.com/Rheinwerk/ansible-role-sshd_trusted_user_ca_setup/actions/workflows/ci.yml/badge.svg)](https://github.com/Rheinwerk/ansible-role-sshd_trusted_user_ca_setup/actions/workflows/ci.yml)

Requirements
------------

The public key of an SSH certificate authority.


Role Variables
--------------

There is one main variable that drives this role: `_sshd_trusted_user_ca_setup`. It is a map that contains all configuration and settings for this role.
Please see `defaults/main.yml` for details.

Dependencies
------------

None.


Example Playbook
----------------

The general contract of this role is to take the variables map `_sshd_trusted_user_ca_setup` from `defaults/main.yml` as a template for your configuration and pass that configuration as a parameter to this role.

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      var:
        sshd_trusted_user_ca_setup:
          ...
      roles:
         - { role: sshd_trusted_user_ca_setup, tags: [ 'sshd_trusted_user_ca_setup' ], _sshd_trusted_user_ca_setup: "{{ sshd_trusted_user_ca_setup }}" }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Daniel Schneller](https://github.com/dschneller) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.

