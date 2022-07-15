# Ansible playbooks for iPharm deployment

## Deployment to test environment with GitHub Actions

You can deploy new docker images to the test environment using 
the "Deploy test..." workflows at https://github.com/conceptica-cz/ipharm-production/actions/workflows/

## Deployment with ansible-playbook

You can deploy new docker images to the demo and production (and also to the test) environment 
using [Ansible](https://docs.ansible.com/ansible/latest/index.html).

### Install ansible

Debian/Ubuntu:

```shell
sudo apt-get install ansible
```

With pip:

```shell
pip install ansible
```

### Clone repository

```shell
git clone https://github.com/conceptica-cz/ipharm-production.git
```

### Deploy

Run one of deploy playbook. For example to deploy ipharm app to the test environment:

```shell
cd ipharm-production
ansible-playbook -i hosts  deploy_test_apache.yml
```



`