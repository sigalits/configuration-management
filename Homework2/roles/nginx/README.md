Role Name
=========

This playbook deploys RedHat/CentOs/Ubuntu servers with Docker Containers with Nginx.

Requirements
------------

The role uses the EC2 module to Deploy servers with tag Name:Node*.

Role Variables
--------------
From Defaults vars:
docker_version: None which means lates version will be deployed , can be overridden using extra-vars

From vars:
install_defalut_dependency: dictionary of lists per ditribution
install_docker_loop :       dictionary of lists per ditribution
docker_users_loop:          dictionary of lists per ditribution  
docker_repos:               dictionary per ditribution 
docker_package: "docker-ce-{{docker_version}}"


Example Playbook
----------------

- name: run over all ec2 servers
   hosts: aws_ec2

  
   roles:
    - nginx


Author Information
------------------

Author: Sigalit Hillel Shelly 
Email : sigalit.hillel@gmail.com
