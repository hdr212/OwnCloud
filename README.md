# OwnCloud 
mkdir example

cd example

vagrant init ubuntu/jammy64

vagrant up --provider=virtualbox

vagrant ssh

sudo -s

apt-get install software-properties-common gnupg2 -y
add-apt-repository ppa:ondrej/php
apt-get update -y
apt-get install php7.4 php7.4-fpm php7.4-cli -y
apt install zip
sudo apt install smbclient redis-server unzip openssl rsync imagemagick
sudo apt install php7.4 php7.4-intl php7.4-mysql php7.4-mbstring \
   php7.4-imagick php7.4-igbinary php7.4-gmp php7.4-bcmath \
   php7.4-curl php7.4-gd php7.4-zip php7.4-imap php7.4-ldap \
   php7.4-bz2 php7.4-ssh2 php7.4-common php7.4-json \
   php7.4-xml php7.4-dev php7.4-apcu php7.4-redis \
   libsmbclient-dev php-pear php-phpseclib


sudo apt install libapache2-mod-php7.4 php7.4-mysql

php -v

apt update

apt upgrade

apt install -y apache2

apt install -y mysql-server

systemctl restart apache2

mysql

CREATE DATABASE bbdd;

CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

GRANT ALL ON bbdd.* to 'usuario'@'localhost';

exit

https://owncloud.com/download-server/
 
Mover el zip a la carpeta

mv /vagrant/owncloud-complete-20230906\(1\).zip /var/www/html/

cd /var/www/html/

ls

unzip owncloud-complete-20230906\(1\).zip

ls

cd owncloud

cp -R * ..

ls

cd ..

ll

ls

rm -r owncloud

rm -r owncloud-complete-20230906\(1\).zip

rm -r index.html

cd /var/www/html

chmod -R 775 .

chown -R root:www-data .

exit

logout

vi Vagrantfile

 config.vm.network "forwarded_port", guest: 80, host: 8080

config.vm.network "public_network"

vagrant reload

vagrant ssh

logout

vagrant reload

vagrant ssh

INICIAR SESION


