Role Name
=========

RHEL8 and RHEL7 Repositories local sync

Requirements
------------

To start the role, please use variables in following way:

rhsm_rhel7_repos:
  - rhel-7-server-rpms
rhsm_rhel8_repos:
  - rhel-8-for-x86_64-baseos-rpms
rhel_additional_software:
  - tmux
rhel_ports_to_open:
  - 22/tcp

If you want to use RHSM for external CDN, please set:

enable_rhsm == True

If you're using your internal Satellite, please set:

enable_rhsm == False


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

Example of playbook starter. 

---
- hosts: rhel-reposync
  gather_facts: yes
  tasks:
  - include_role:
      name: rhel-reposync
    vars:
      enable_rhsm: True
      rhsm_username: rhsm_username
      rhsm_password: rhsm_password
      rhsm_pool_id: pool_id

Also, please check for default variables to set up repositories and default repo directory.


License
-------

BSD

Author Information
------------------

email: dalekhin@redhat.com
