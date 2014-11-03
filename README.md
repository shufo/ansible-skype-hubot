ansible-skype-hubot
===================

A playbook for skype and hubot integration on CentOS.

## Overview

It will install skype and hubot on CentOS. You can customize it by edit vars file.

## Usage

Replace username/password with your skype credential.

- vars/main.yml

```vars/main.yml
skype_username: your_skype_id
skype_password: your_skype_password
```

- Run playbook.

```bash
ansible-playbook site.yml
```

## vars

```vars/main.yml
skype_version: 4.3.0.37
skype_install_dir: /opt/skype
skype_init_script: /etc/init.d/skype
skype_username: your_skype_id
skype_password: your_skype_password

hubot_install_dir: /opt/hubot

```

## Vagrant

You can test on Vagrant virtual machine.

```
vagrant up
```

## Note

Skype Desktop API was deprected in December, 2013, so cloud based group created in 2014 unable to use hubot.
Still Dialog chat and P2P group created before 2013 is able to use hubot.

On old chats:

```
/get name
name=#reiner030/$martin.somewhere;dab11af9c767e33
```

still API is alive.

On new chats:

```
/get name
name=19:ebcb1d256736467d9c38332b131ca675@thread.skype
```

can't use API.

refs : https://github.com/awahlig/skype4py/issues/34
