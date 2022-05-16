# Ansible-Ontap-Setup
Setup and Configure NetApp Cluster pre-cluster mode

################################################

This repo include serveral files to initialize cluster setup

## 'vars' folder
contain var.yml file with all the variables to use the playbook

## 'tasks' forlder
contains 2 files, one for cluster setup and the second for configuration includes Aggregate creation, Volumes, luns etc...

# How to Run?
```
 ansible-playbook ConfigCluster.yml -e=@../vars/vars.yml
```
 
 can also use --tags='sometag' to run specific tasks, the task must include the following format:
```
 - name: Some Task
   na_ontap_volume:
   ...
   tag:
     - 'sometag'
```
  # Use at you work risk!!
