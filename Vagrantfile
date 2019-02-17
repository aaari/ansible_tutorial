# -*- mode: ruby -*-

Vagrant.configure("2") do |config|
  config.vm.define "controller" do |node|
        node.vm.box = "centos7.2"
        node.vm.hostname = "controller"
        node.vm.network :private_network, ip: "192.168.100.10"
        node.vm.network :forwarded_port, id: "ssh", guest: 22, host: 2210
        node.vm.synced_folder "./shared", "/home/vagrant/shared", owner: "vagrant", group: "vagrant"
  end
  config.vm.define "target" do |node|
        node.vm.box = "centos7.2"
        node.vm.hostname = "target"
        node.vm.network :private_network, ip: "192.168.100.20"
        node.vm.network :forwarded_port, id: "ssh", guest: 22, host: 2220
  end
end
