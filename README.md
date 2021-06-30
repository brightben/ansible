# ansible test scripts

## Run ansible
ansible-playbook test.yml
ansible-playbook test.yml --tags first_tag

## List available running ansible tasks
ansible-playbook test.yml --list-tasks
ansible-playbook test.yml --tags first_tag --list-tasks

## List hosts gathering facts
ansible all -m setup -i inventories -a "filter=ansible_lsb"
var -> {{ ansible_facts['lsb'] }} 
