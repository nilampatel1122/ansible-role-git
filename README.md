Role Name
=========

A role to install and configure git.

Requirements
------------

None.

Role Variables
--------------

```yaml
---
# Git packages. By default only git is installed.
# But for example it can be changed to git-all.
git_packages:
  - git

# List of git configuration. Scope is system or global
# and the default value is global.
# Example:
# git_config:
#   - name: user.name
#     value: My name
#     scope: global
#   - name: user.email
#     value: myemail@mail.com
#     scope: global
git_config: []

# Global git configuration will be added to home directroy
# of this user: ~/.gitconfig
git_user: root

```

Dependencies
------------

None.

Example Playbook
----------------

playbook.yml
```yaml
- hosts: servers
  become: true
  roles:
    - role: siavashoutadi.git
```
And run like this:
```shell
ansible-playbook -i inventory -K playbook.yml
```

License
-------

Apache 2.0.

Author Information
------------------

Siavash Outadi.
