Role Name
=========

A small example of an ansible playbook to work with Windows 10

Requirements
------------

* Need to install "Chocalatey"

Role Variables
--------------
All variables are in inventory, you may need to use "become"
```
[all:vars]
ansible_connection=winrm
ansible_port=5985 
ansible_user=vagrant
ansible_password=vagrant
ansible_winrm_server_cert_validation=ignore
```
Dependencies
------------
* ansible_chocolatey
* winrm setup for http and https (if domain and valid certificate)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- name: Setup software deployement
  hosts: all

  tasks:
    - name: deploying software for Windows
      include_role:
        name: roles/software
```

Author Information
------------------

[Pullyvan Krishnamoorthy](pullyvan.kris@gmail.com)
