#Dolly#
![Dolly](http://www.animalresearch.info/files/7414/0742/1258/1996_1.jpg)

For testing of [satellite-clone](https://github.com/RedHatSatellite/satellite-clone) 

##Prerequisites##
- A blank RHEL 7 machine that has access to yum repos, referred to as blank_testing_machine

##Quick Setup##
1. `ssh-copy-id root@<blank_testing_machine>`
2. `cp inventory.sample inventory` and update with the blank_testing_machine fqdn or ip
3. move your satellite-clone-vars.yml file to `roles/setup/files`
4. move your satellite-hostname-vars.yml file to `roles/setup/files`
5. `cp setup-vars.sample.yml setup-vars.yml` and update as necessary
6. `ansible-playbook -i inventory test-clone.yml`
