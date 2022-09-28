ansible run playbook
1) if ansible is not installed
  a)sudo apt update
  b)sudp apt install ansible
2) clone this repo
  git clone https://github.com/maxmosua/anstest.git
3) run playbook 
   ansible-playbook site.yml

playbook consists of 5 roles:
     - initiate (change ssh port, configuration csf with variables in group_vars/all.yml)
     - nginx (install nginx, configure virtual host)
     - php-fpm (install php8.1-fpm and its dependencies )
     - mysql (install mysql-server, configure access,create database for wordpress)
     - wordpress (download archive with the latest version, configuration file wp-config.php)
     - logrotate (logrotate service configuration for nginx, php-fpm, mysql-server)
     
Unfortunately, I did not have time to set up monitoring, lets ecnrypt cert and backup ((
