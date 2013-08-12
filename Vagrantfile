# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. 
# Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
  config.vm.box = "nodejs-precise32-0.0.1"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "http://cdn.junwatu.com/files/vagrant/nodejs/nodejs-precise32-0.0.1.box"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  
  config.vm.network :forwarded_port, guest: 80, host: 8085, auto_correct:true
  config.vm.network :forwarded_port, guest: 27017, host: 27117

  config.vm.provision :shell, :path => "update.sh"

end
