Ansible Role: install-kube
=========

Ansible Role for preparing and installing kubernetes on multiple machines using Ansible.

Requirements
------------
No special requirements; note that this role requires root access, so either run it in a playbook with a global become: yes, or invoke the tasks in your playbook like:
```
- hosts: servers
  tasks:
    - name: install-kube
      import_role:
        name: ansible-role-install-kube
      become: yes
```
installing
------------
Inside the same folder your playbook is in:
```
mkdir -p roles
cd roles
git clone https://github.com/hiitsmatan/ansible-role-install-kube.git
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- hosts: all
  become: yes
  tasks:
    - name: install kube
      import_role:
        name: ansible-role-install-kube
```
