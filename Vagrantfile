# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.forward_port 8888, 8888

  config.ssh.forward_x11 = true

  config.vm.provision :puppet do |puppet|
    puppet.manifest_file  = "vagrant.pp"
    puppet.manifests_path = "puppet/manifests"
    puppet.module_path    = "puppet/modules"
    #puppet.options = "--verbose --debug"
  end
end
