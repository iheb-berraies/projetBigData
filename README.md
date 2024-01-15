# Kubernetes the Hard Way with Vagrant, VirtualBox, kubectl, Ansible, and ngrok

## Overview

This repository provides a Vagrant-based environment for deploying Kubernetes the hard way. It is intended for local development and testing purposes, allowing you to understand the manual steps involved in setting up a Kubernetes cluster.

## Prerequisites

Before you begin, ensure that you have the following software installed on your local machine:

- [Vagrant](https://www.vagrantup.com/)
- [VirtualBox](https://www.virtualbox.org/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- [ngrok](https://ngrok.com/)

## Getting Started

1. **Clone this repository:**

   ```bash
   git clone https://github.com/iheb-berraies/projetBigData
   cd kubernetes-the-hard-way
   

2. *Launch the Vagrant environment:*

   
   cd kubernetes-the-hard-way
   vagrant up
   

   This command sets up the virtual machines required for the Kubernetes cluster.

3. **Access the deploy-kube-features directory:**

   
   cd deploy-kube-features
   

4. *Run the Ansible playbook to deploy Kubernetes features:*

   
   ansible-playbook -i inventories/DEV/host.ini playbook.yaml --ask-vault-password
   

   When prompted for the vault password, enter: test.

## Notes

- This setup is intended for local development and testing purposes.
- For security reasons, it's recommended to change the default passwords and secrets in a production environment.
- Ensure that your machine meets the minimum requirements for running a Kubernetes cluster.

## Troubleshooting

If you encounter any issues during the setup, refer to the [troubleshooting guide](docs/troubleshooting.md) for common solutions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```
