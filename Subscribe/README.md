# Subscribe.yml
Subscribes and attaches RHEL systems using subscription-manager

To run this playbook:
  1. Have a group of hosts in your inventory to act upon.
  2. Have a username and password for the RH portal.
  3. ansible-playbook Playbooks/Subscribe/Subscribe.yml -i hosts.ini --extra-vars '{ "username":"yourusername", "password":"yourpassword", "hosts":"rhel" }' -K
       - BECOME password: becomepassword
       - The password is used for sudo execution, not su, so this play must be run by a user with sudo permission
