# digitalocean-ansible-drupal

$ git config user.email "matt@obj-a.com"
$ git config user.name "obja"

To add aliases to your profile:
$ cp -rfp profileia/.bash_aliases ~/

To install pip and ansible via pip (recommended), just go into drupal_setup:
$ ./install_ansible.sh

For Drupal 8 run:
$ ansible-playbook 8site.yml
For Drupal 7 run:
$ ansible-playbook 7site.yml

After installing Drupal 8 fully run:
$ ansible drupal_hosts -m file -a "dest=/var/www/html/sites/default/settings.php mode=644"
and
$ ansible drupal_hosts -m file -a "dest=/var/www/html/sites/default/services.yml mode=644"
For Drupal 7 just do the first command.
