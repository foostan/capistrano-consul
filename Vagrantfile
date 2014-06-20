# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network :private_network, ip: "192.168.33.10"

  config.vm.provision "shell", inline: <<-EOS
    sudo apt-get -y update
    sudo apt-get install -y git apache2
    sudo chown vagrant:vagrant /var/www -R
  EOS
end
