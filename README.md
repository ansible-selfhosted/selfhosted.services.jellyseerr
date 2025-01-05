[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border.json)](https://github.com/copier-org/copier)
[![Podman Badge](https://img.shields.io/badge/Podman-892CA0?logo=podman&logoColor=white)](https://podman.io/)
[![Hatch project](https://img.shields.io/badge/%F0%9F%A5%9A-Hatch-4051b5.svg)](https://github.com/pypa/hatch)
![CI](https://github.com/ansible-selfhosted/selfhosted.services.jellyseerr/actions/workflows/ci.yml/badge.svg)
[![Ansible](https://img.shields.io/badge/Ansible-Molecule-EE0000?style=plastic&logo=ansible&logoColor=white)](https://github.com/ansible/molecule)

<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: [jellyseerr](https://docs.jellyseerr.dev/)

A role to deploy Jellyseerr using rootless Podman with systemd

## Role Requirements

- none

*Refer to services collection for general requirements*

## Role Arguments

|Option|Description|Type|Required|Default|
|---|---|---|---|---|
|jellyseerr_additional_options|List of additional key=value for the quadlet container<br>ex: - "Network=custom.network"<br>Can also be used to leave comments by preceding with a '#'|list|False|[]|
|jellyseerr_config_label|The labels for to the jellyseerr config directory<br>Comma separated values (ex: rw,Z)|str|False||
|jellyseerr_config_path|The path to the jellyseerr configuration directory|str|False|~/.config/jellyseerr/|
|jellyseerr_timezone|The timezone for the jellyseerr service|str|False|Etc/UTC|
|jellyseerr_version|The version of jellyseerr container|str|False|latest|
|jellyseerr_web_port|The port for the web server|int|False|5055|


## Example Playbook

```
- hosts: all
  tasks:
    - name: Importing jellyseerr role
      ansible.builtin.import_role:
        name: selfhosted.services.jellyseerr
      vars:
```

## License

This project is licensed under the [MIT License](LICENSE)


⊂(▀¯▀⊂)

<!-- END_ANSIBLE_DOCS -->
