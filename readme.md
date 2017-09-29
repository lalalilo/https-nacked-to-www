# Ansible playbook to setup a redirection server from your root domain name to wwww subdomain using Let's encrypt on nginx.

The Ansible playbook installs nginx and let's encrypt to redirect https://example.com to https://www.example.com.

This repository is an adaptation of https://gist.github.com/mattiaslundberg/ba214a35060d3c8603e9b1ec8627d349

To use:
 1. Install [Ansible](https://www.ansible.com/)
 2. Setup an Ubuntu 16.04 server accessible over ssh
 3. Adjust the variables in inventories/production
   - example.com => yourdomain.com
   - letsencrypt_email => the email that will be linked to the SSL certificat
   - ansible_ssh_private_key_file => the SSH key to connect to the remote server
 4. Run `ansible-playbook playbook.yml -i inventories/production`
