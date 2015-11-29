# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/wily64"
  config.vm.network "private_network", ip: "192.168.33.11"
  config.vm.synced_folder "/home/aramonc/Projects/sig-ops", "/home/vagrant/sig-ops"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
    vb.cpus = 2
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/php_cli.yml"
  end
end
