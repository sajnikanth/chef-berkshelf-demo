# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "saucy64"
  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.omnibus.chef_version = 'latest'
  config.vm.provision :chef_solo do |chef|
     chef.cookbooks_path = "./cookbooks"
     chef.add_recipe "nginx"
     chef.add_recipe "apt"
  end
end
