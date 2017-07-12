# encoding: utf-8
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.box = 'centos/7'
  config.vm.hostname = 'chef.dev.tmg.net'
  config.vm.network 'private_network', type: 'dhcp'
  config.vm.provider 'virtualbox' do |vb|
    vb.memory = 2048
    vb.cpus = 2
  end
  config.berkshelf.enabled = true
  config.vm.provision 'chef_solo' do |chef|
    chef.add_recipe 'chef-server'
  end
end
