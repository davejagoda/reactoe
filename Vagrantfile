# -*- mode: ruby -*-
# vi: set ft=ruby :

HOSTNAME = 'reactoe'
VAGRANTFILE_API_VERSION = '2'
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.forward_agent = true
  config.vm.box = 'ubuntu/bionic64'
  config.vm.hostname = HOSTNAME
  config.vm.provider 'virtualbox' do |vb|
    vb.name = HOSTNAME
  end
  config.vm.network 'forwarded_port', guest: 3000, host: 3000
  config.vm.provision 'shell', inline: 'apt-get update'
  config.vm.provision 'shell', inline: 'apt-get install -y npm'
end
