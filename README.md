# CentOS 8 Docker Image for Ansible Testing

DEPRECATED - CentOS Linux 8 is End Of Life (EOL) as of December 31st 2021. For alternatives please see the below.

  - [AlmaLinux 8](https://github.com/glillico/docker-almalinux8-ansible)
  - [Oracle Linux 8](https://github.com/glillico/docker-oraclelinux8-ansible)
  - [Rocky Linux 8](https://github.com/glillico/docker-rockylinux8-ansible)

[![latest](https://github.com/glillico/docker-centos8-ansible/workflows/latest/badge.svg)](https://github.com/glillico/docker-centos8-ansible/actions?query=workflow%3Alatest)

A docker container using CentOS 8 with Ansible installed for playbook and role testing.

## Tags

  - 'latest'  : Python 3.6.x and the latest stable version of Ansible.

## How To Build

To build this docker container you can do the following.

  - Install Docker Engine, see [here](https://docs.docker.com/engine/install/) for details.
  - Clone this repository.
    - `$ git clone https://github.com/glillico/docker-centos8-ansible.git`
  - Change to the repositories directory.
    - `$ cd docker-centos8-ansible`
  - Run the command
    - `$ docker build -t centos8-ansible .`

## How To Use

  - Install Docker Engine, see [here](https://docs.docker.com/engine/install/) for details.
  - To create a containter from the image you created in the `How To Build` section run the command.
    - `$ docker run --detach --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro centos8-ansible:latest`
  - To confirm Ansible is working within the container run the command.
    - `$ docker exec --tty <CONTAINER ID> env TERM=xterm ansible --version`

## Notes

This image is used for testing purposes only and is not intended to be used to provide live services of any sort.

## License

MIT

## Author Information

Created in 2020 by Graham Lillico.
