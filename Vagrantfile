# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "debian/bullseye64"
  config.vm.network "public_network", dev: "br0", ip: "192.168.178.106"
  
  #config.vm.define "shelf"
  #config.vm.hostname= "shelf"
  
  # Perform basic configuration of the VM:
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook_base.yml"
  end

  # Perform app specific configuration of the VM:
  #config.vm.provision "ansible" do |ansible|
  #  ansible.verbose = "v"
  #  ansible.playbook = "app/playbook.yml"
  #end
end
