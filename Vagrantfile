# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.define :web do |web_config|
      web_config.vm.box = "hashicorp/precise64"
      web_config.vm.network :private_network, ip: "192.168.33.10"
      web_config.vm.network "forwarded_port", guest: 80, host: 8080
      web_config.vm.provision :shell, path: "bootstrap.sh"
  end
  config.vm.define :db do |db_config|
      db_config.vm.box = "hashicorp/precise64"
      db_config.vm.network :private_network, ip: "192.168.33.11"
  end

  config.vm.define :file do |file_config|
      file_config.vm.box = "hashicorp/precise64"
      file_config.vm.network :private_network, ip: "192.168.33.12"
  end

end
