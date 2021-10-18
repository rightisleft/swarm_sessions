# Pienso Ansible Modules
This will boostrap and manage docker swarm nodes

* This tests Centos 7
* This tests Ubuntu 18.04

Ensure you are running 

```
  ansible-galaxy [core 2.11.4]
  config file = /Users/jmurphy/projects/anzi/ansible.cfg
  configured module search path = ['/Users/jmurphy/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/Cellar/ansible/4.5.0/libexec/lib/python3.9/site-packages/ansible
  ansible collection location = /Users/jmurphy/.ansible/collections:/usr/share/ansible/collections
  executable location = /usr/local/bin/ansible-galaxy
  python version = 3.9.7 (default, Sep  3 2021, 12:37:55) [Clang 12.0.5 (clang-1205.0.22.9)]
  jinja version = 3.0.1
  libyaml = True
```

### Start VMS
```
cd ~/anszi/vms
vagrant up
```

### Install Modules
```
cd ~/anszi
ansible-galaxy install -r requirements.yml
```

### Run Playbook
```
ansible-playbook -i hosts.yml playbook.yml
```

### Clean VMS
```
cd ~/anszi/vms
vagrant destroy --force
```
