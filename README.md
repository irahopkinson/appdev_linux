# Linux AppDev Development Setup #

[![Build Status](https://travis-ci.org/irahopkinson/appdev_linux.svg?branch=master)](https://travis-ci.org/irahopkinson/appdev_linux)

Install and configure development environment for developing AppDev plugins.

At the moment (2016 Feb 4) Ansible v2.0.0.2 is [broken on local connections](https://github.com/ansible/ansible/issues/13763). Install v1.9 instead:
````
sudo apt-get install python-pip
sudo pip install ansible==1.9.4
````

You may need to install Ansible role [geerlingguy.nodejs](https://galaxy.ansible.com/detail#/role/465).

Copy to a **deploy** folder or clone...
```
git clone https://github.com/irahopkinson/appdev_linux.git deploy
```
then...

```
cd deploy
ansible-playbook -i hosts playbook_appdev.yml --limit localhost -K
```

## License ##

Licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
