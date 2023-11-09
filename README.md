# Firewall config role

This role configures rules for UFW and firewalld.

## Requirements

`netaddr` on Ansible controller.

## Example dependency

```yml
dependencies:
  - name: cosandr.firewall_config
    src: https://github.com/cosandr/ansible-role-firewall-config.git
    scm: git
    version: v1.0.0
```

## Example Playbook

```yml
- hosts: servers
  roles:
    - role: cosandr.firewall_config
      vars:
        firewall_rules:
          - port: 9100
            sources: ["10.0.10.11", "10.0.10.12", "10.0.10.13"]
```

## License

MIT

## Author Information

Andrei Costescu
