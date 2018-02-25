# Ansible : Playbook Mattermost
The aim of this project is to deploy a simple Mattermost instance on Vagrant with Postgresql backend.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What things you need to run this Ansible playbook :

* [Vagrant](https://www.vagrantup.com/docs/installation/) must be installed on your computer
* Update the Vagrant file based on your computer (CPU, memory), if needed
* You must have download the ubuntu Xenial64 vagrant box :

```
vagrant box add https://app.vagrantup.com/ubuntu/boxes/xenial64
```

### Usage

A good point with Vagrant is that you can create, update and destroy all architecture easily with some commands.

Be aware that you need to be in the Vagrant directory to be able to run the commands.

#### Build Environment

Vagrant needs to init the project to run and build it :

```
vagrant up
```

After build, you can check which virtual machine Vagrant has created :

```
vagrant status
```

If all run like it is expected, you should see something like this :

```
$ vagrant status

Current machine states:

mattermost01                  running (virtualbox)
```

#### Deployment

To deploy the Mattermost instance, you just have to run the Ansible playbook mattermost.yml with this command :

```
ansible-playbook mattermost.yml
```

If all run like it is expected, you should access Mattermost Web interface : http://10.0.1.61:8065/

#### Destroy

To destroy on what Vagrant has created, just run this command :

```
vagrant destroy
```

## Author

Member of Wikitops : https://www.wikitops.io/
