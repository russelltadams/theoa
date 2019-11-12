# theoa

## Description
An Ansible playbook to install Openarena with Excessiveplus on Ubuntu 16.04. It might work on 14.04 or Debian, as well, but I have not tested there yet, give it a try, let me know how it goes. My main use case is using it in the cloud where almost all providers have 16.04 as an option with cheap affordable VM sizes. OA server needs very little resources to run!

The playbook installs a generic but useful 'free for all' OA server that includes a map rotation script that adjusts to the number of players on the server. You can of course change everything as needed on the server or edit the playbook to install your own map rotation. In the future this playbook should be made into a more generic role that supports more custom configurations. But for now I am using a configuration that suits my use, 'Free For All' with a nice auto scaling map rotation script.

The game is started with the shell module in a screen session call "theoa" so you can easily get to the server console and interact with it if needed or just let it run in the background.

## Instructions

Coming soonish...

### Install requirements

Coming soonish...

### Run the playbook
ansible-playbook theoa.yml -i inventory/all --diff -vv -u root

# To-Do
* find more good maps (and player number sizes) for rotation.txt
* make rotation.txt a jinja2 template so the maps can be variables
* figure out some decent settings to varableize for exceessiveplus
* try to make playbook --check --diff safer
* bust out roles, allow more custmization
