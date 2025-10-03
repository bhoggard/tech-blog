+++
date = '2025-10-02T23:22:56-04:00'
draft = false
title = 'Setting up Vagrant and VirtualBox on Pop!_OS or Ubuntu 22'
+++

When I started to set up Vagrant and VirtualBox on my Pop OS Linux machine, I had trouble with conflicting versions of Vagrant and VirtualBox. The version of Vagrant available via `apt install` wasn't compatible with the version of Virtualbox installed with apt.

I solved it by removing vagrant, then installing VirtualBox normally using apt.

```bash
sudo apt update
sudo apt remove vagrant
sudo apt install virtualbox
```

I then installed the official Vagrant package from [Hashicorp](https://developer.hashicorp.com/vagrant/install). In my case I used:

```bash
wget https://releases.hashicorp.com/vagrant/2.4.1/vagrant_2.4.1-1_amd64.deb
sudo apt install ./vagrant_2.4.1-1_amd64.deb
```
