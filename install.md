# ubuntu-install-mongodb
Step 1: Add package

sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5

echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.6.list

Step 2: 
sudo apt-get update
sudo apt-get install -y mongodb-org
 
End: Add driver php mongo
$ git clone https://github.com/mongodb/mongo-php-driver.git
$ cd mongo-php-driver
$ git submodule update --init
$ phpize
$ ./configure
$ make all
$ sudo make install
