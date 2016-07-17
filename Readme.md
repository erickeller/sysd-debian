# systemd tests

This repository contains a simple systemd test where one has to install two services

# Prerequisites

```
sudo apt-get update && sudo apt-get install vagrant lxc
vagrant plugin install vagrant-lxc
```

# usage

```
vagrant up --provider lxc --provision
vagrant ssh
cd /vagrant
debuild -uc -us
dpkg -i ../*.deb
# verify the services are enabled
sudo systemctl is-enabled sysd-debian-backend.service
sudo systemctl is-enabled sysd-debian.service
```


