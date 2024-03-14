# ansible-sshd_config

Ansible role to configure SSH daemon on debian

## Getting started

Install into your project with ansible-galaxy

```shell
ansible-galaxy install --roles-path ./roles git+https://github.com/haukurh/ansible-sshd_config.git
```

... or you can just use git, submodules or what ever you find most convenient

```shell
git clone https://github.com/haukurh/ansible-sshd_config.git roles/sshd_config
```

## Ansible role

folder structure

```
sshd_config/
    tasks/              #
        main.yml        #  <-- tasks file can include smaller files if warranted
    handlers/           #
        main.yml        #  <-- handlers file
    templates/          #  <-- files for use with the template resource
        sshd_config.j2  #  <------- templates end in .j2
    files/              #
        bar.txt         #  <-- files for use with the copy resource
        foo.sh          #  <-- script files for use with the script resource
    vars/               #
        main.yml        #  <-- variables associated with this role
    defaults/           #
        main.yml        #  <-- default lower priority variables for this role
    meta/               #
        main.yml        #  <-- role dependencies
    library/            # roles can also include custom modules
    module_utils/       # roles can also include custom module_utils
    lookup_plugins/     # or other types of plugins, like lookup in this case
```

- [docs.ansible.com: Roles](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_reuse_roles.html)
