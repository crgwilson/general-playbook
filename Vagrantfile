# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.define 'testing' do |testing|
    testing.vm.box = 'centos/7'
    testing.vm.hostname = 'test-host'

    testing.vm.provider :virtualbox do |v|
      v.memory = '1024'
      v.cpus = '1'
    end

    testing.vm.provision :ansible do |a|
      a.playbook = 'site.yml'
      a.extra_vars = {
        ansible_user: 'vagrant'
      }
    end
  end
end
