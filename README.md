# ansible-vps-setup

Contains several ansible roles to configure a new VPS (DO Droplet)

## Usage
Install ansible on server directly or on a control machine ([Read how in docs](http://docs.ansible.com/ansible/intro_installation.html))

To install ansible on server directly (Ubuntu ^14.0.0)
```
apt-add-repository ppa:ansible/ansible -y
apt-get update
apt-get install ansible
```

If you use the server as control machine you need to transfer the files to /etc/ansible/

Using vault requires a vault_pass file in /etc/ansible. Name and path can be changed in ansible.cfg

## Roles

* Security - Contains iptables to set up highsecurity rules for your server, also disables password authentication
* User setup - Creates users based on small user config files (see kim_user.yml)
* NTP - Installs ntp and set correct timezone for server
* nodejs - Fetches node binaries and sets PATH variables, creates a node user in meta
* nginx - Installs nginx and defines default site-available/-enabled with stricter restrictions (from nexi)
* mysql - Installs mysql-server, configures securely and creates a new mysql user with new database setting proper privileges


