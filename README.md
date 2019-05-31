# Kubernetes deploy ansible

This project  provisions of kubernetes cluster. Provisioning is done with ansible playbook.

### What this project accomplishes in details:
- Installs docker on each host
- Installs and configures Kubernetes on each node
- Performs cluster init on master
- Joins workers to cluster




### Initial setup for ansible

#### Using ansible with custom inventory
In order to use inventory add hosts to `dev.inventory` file with the following groups:
```
[kubernetes-master]
[kubernetes-workers]
[mysql]
```

Run playbook specifying hosts file:
- `ansible-playbook -i dev.inventory --ask-vault-pass`

### Running Playbook
- `ansible-playbook --ask-vault-pass dev.yaml`
