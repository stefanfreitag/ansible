# README

## Commands

```shell
ansible-galaxy collection install kubernetes.core 
```

Playbooks:

- `playbooks/software_packages_kubuntu.yml` - installs common packages on Kubuntu (uses `apt`). Run with an inventory that defines the `kubuntu` host/group.
- `playbooks/software_packages_fedora42.yml` - installs common packages on Fedora 42 (uses `dnf`). Run with an inventory that defines the `fedora42` host/group.

Example commands (run from repository root):

```shell
ansible-playbook -i inventory.ini playbooks/software_packages_kubuntu.yml --limit kubuntu
ansible-playbook -i inventory.ini playbooks/software_packages_fedora42.yml --limit fedora42
```