# Create a Hetzner snapshot using Packer - provisioning using Ansible
This project:
* Uses [Packer](https://www.packer.io/docs) to create a snapshot.
* Provision using [Ansible](https://docs.ansible.com/ansible/latest/index.html)
  * update packages
  * add non-root user with a custom SSH key
  * install docker

The snapshot can then be used to quickly stand a cluster using Terraform

You can customize the Ansible playbook to do more customisations.

## Usage
* Install [Packer](https://www.packer.io/docs/install) and [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) 
* Get an API token from Hetzner Cloud
* Set Hetzner token environment variable `export HCLOUD_TOKEN=xxx`
* Customize packer.json
* Customize the Ansible playbook
* Run packer to create the snapshot

```bash
packer build packer.json
```

