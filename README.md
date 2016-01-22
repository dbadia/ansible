These are ansible playbooks for setting up MythTV buildslaves.

How to use this
# git clone https://github.com/MythTV/ansible

Debian users will need to enable wheezy-backports
https://wiki.debian.org/Backports

Then install the `ansible` package. Choose the one appropriate
for your distro
# yum install ansible
# dnf install ansible
# apt-get install ansible
# pacman -S ansible python2

Then run the playbooks as follows.

Please note archlinux users will need to add `--limit archlinux` to these commands

For a normal development system running Qt4
# ansible-playbook -i hosts qt4.yml

For a normal development system running Qt5
# ansible-playbook -i hosts qt5.yml

For a buildslave system running Qt4
# ansible-playbook -i hosts buildslave.yml

For a buildslave system running Qt5
# ansible-playbook -i hosts buildslave-qt5.yml

For a buildslave system running both Qt4 and Qt5
# ansible-playbook -i hosts buildslave.yml
