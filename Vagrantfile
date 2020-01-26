# -*- mode: ruby -*-
# vi: set ft=ruby :

#ENV['VAGRANT_NO_PARALLEL'] = 'yes'

Vagrant.configure(2) do |config|

  # Ceph-controller
  config.vm.define "vag" do |vag|
    vag.vm.box = "centos/7"
    vag.vm.hostname = "vag"
    vag.vm.network "public_network",
      use_dhcp_assigned_default_route: true
    vag.vm.provision "ansible", playbook: "localhost_playbook.yml"
    vag.vm.provider "virtualbox" do |v|
      v.name = "vag"
      v.memory = 1024
      v.cpus = 1
    end
  end
end
