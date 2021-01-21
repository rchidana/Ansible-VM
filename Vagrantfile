# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.box_check_update = false
  
  config.vm.provider :virtualbox do |vb|
   vb.customize ["modifyvm", :id, "--memory", "256"]
  end

# Controller.
 config.vm.define "ansible-controller" do |cont|
	cont.vm.hostname = "ansible-controller"
	cont.vm.box = "geerlingguy/ubuntu1604"
	config.vm.box_download_insecure = true
	config.vm.network "public_network"
	cont.vm.network "private_network", ip: "192.168.60.60"
 end

end 
