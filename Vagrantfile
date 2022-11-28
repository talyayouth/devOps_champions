# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"

  config.vm.box_check_update = false
  config.vm.provider "virtualbox" do |vb|
    vb.name = "new_app"
    vb.memory = "1024"
    vb.cpus = 1
  end

  config.vm.hostname = "new_host"

  config.vm.synced_folder "C://{directory}//devOps_champions", "/devOps_champions", disabled: true

  config.vm.network "forwarded_port", guest: 80, host: 8000

  config.vm.network "private_network", ip: "192.168.10.100"

  config.vm.provision "shell", path: "provision.sh"
end
