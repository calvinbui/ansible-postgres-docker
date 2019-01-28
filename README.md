# Ansible Postgres Docker

Run Postgres inside a Docker container

##  Requirements

N/A

## Role Variables

`postgres_docker_tag`: Docker tag found at https://hub.docker.com/_/postgres

`postgres_docker_network`: Dictionary of Docker networks following https://docs.ansible.com/ansible/latest/modules/docker_container_module.html. Leave empty `[]` to not use it

`postgres_docker_exposed_ports`: List of exposed ports. Leave empty `[]` to not use it

`postgres_docker_data_dir`: Where to store data

`postgres_docker_user`: This variable is used in conjunction with POSTGRES_PASSWORD to set a user and its password. This variable will create the specified user with superuser power and a database with the same name.

`postgres_docker_password`: Sets the superuser password for PostgreSQL

`postgres_docker_database`: Default database that is created when the image is first started

## Dependencies

- Docker

## Example Playbook

```yaml
- hosts: servers
  become: true
  roles:
    - role: calvinbui.ansible_docker
    - role: calvinbui.ansible_postgres_docker
```

## License

GPLv3

## Author Information

http://calvin.me
