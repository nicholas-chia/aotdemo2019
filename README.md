
1. Edit extra_vars.yml and update with needed credentials
# tower credential
towuser: admin
towpass: ansible

# managed nodes credential
machinesshuser: student1
machinesshpass: ansible

# insights scm credential
rhnuser: ChangeMe
rhnpass: ChangeMe

# student number given by rhpds for ssh
studentid: student1

2. Use ansible-vault to protect your extra_vars.yml file
$ ansible-vault encrypt extra_vars.yml

3. Run Ansible Playbook to setup demo
$ ansible-playbook setup-aotdemo-tower.yml -e @extra_vars.yml --ask-vault-pass -v
