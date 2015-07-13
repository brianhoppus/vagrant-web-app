# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "puppetlabs/centos-6.6-64-puppet"


  config.vm.define "loadbalancer" do |lb|
      lb.vm.hostname = "loadbalancer.fake.local"
      lb.vm.network "forwarded_port", guest: 80, host: 8080
      lb.vm.network "private_network", ip: "192.168.1.10"
  end

  config.vm.define "apache1" do |web|
      web.vm.hostname = "apache1.fake.local"
      web.vm.network "private_network", ip: "192.168.1.11"
  end

  config.vm.define "apache2" do |web|
      web.vm.hostname = "apache2.fake.local"
      web.vm.network "private_network", ip: "192.168.1.12"
  end

  config.vm.define "apache3" do |web|
      web.vm.hostname = "apache3.fake.local"
      web.vm.network "private_network", ip: "192.168.1.13"
  end
end
