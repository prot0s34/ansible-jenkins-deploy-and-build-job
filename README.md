# ansible-jenkins-deploy-and-build-job
Automate Jenkins Install, Import &amp; Run Free Job

This playbook install Jenkins and sshpass to LAB-VM01, import job from XML file to jenkins and automatically run first jenkins job.

sw versions:
ansible 2.9.6
LAB-VM01:CentOS-8.4.2105-x86_64
LAB-VM02:CentOS-8.4.2105-x86_64
Jenkins:latest


Lab task: Setting up two servers. VM OS - CentOS. 

On LAB-VM01: Install & Configure Jenkins with ansible-playbook.
Then create Free Plan Job in Jenkins (job run on Jenkins master LAB-VM02 and configure LAB-VM02 via remote shell
 
Configuration for LAB-VM02

- Install packages: htop, tmux, jq
- configure sshd service:
  - PermitRootLogin no
  - PasswordAuthentication no
  - sshpass jenkins .pub key for non-password authentication
  - restart sshd service

There is two files - lab01.yml playbook and job in .xml for import and run in jenkins (bash configure ssh and remote node LAB-VM02)
