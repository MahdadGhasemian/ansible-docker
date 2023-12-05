# Ansible Role: Docker

Installs Docker for Debian/Ubuntu linux servers.

## Requirements

None.

## Role Variables

# Service options.
docker_service_manage: true
docker_service_state: started
docker_service_enabled: true
docker_restart_handler_state: restarted

# Container
container_count: 1
default_container_name: hello
default_container_image: hello-world
default_container_command: sleep 1d

## Dependencies

- community.docker

## Example Playbook (using default package)

    - hosts: servers
      roles:
        - role: MahdadGhasemian.ansible-docker
          become: yes

## License

MIT / BSD

## Author Information

This role was created in 2023 by [Mahdad Ghasemian](https://mahdad.me/).