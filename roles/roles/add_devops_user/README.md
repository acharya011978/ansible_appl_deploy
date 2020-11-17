Ansible-Sample-Application-Deployment
This repository will contain sample code to deploy the sample application on linux instance

Directory Structure
configs - contain environment specific variable

inventories - contains inventory file for each environment

groups_vars - contains common variables across environments

a) add_devops_user - This folder will have files related to the setup of initial user

main.yml - This is the main file which will execute roles in the playbook

How to Run the Playbook

ansible-playbook main.yml -i inventories/dev/hosts --user ec2-user --key-file /home/ec2-user/playbooks/ansible_aut.pem -e '@configs/dev.yml'

ansible-playbook main.yml -i inventories/dev/hosts --user devops --key-file /home/devops/.ssh/id_rsa -e '@configs/dev.yml'
