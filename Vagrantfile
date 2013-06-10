# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Standard Ubuntu 12.04.2 base box
  config.vm.box = "ubuntu-12.04.2-amd64"
  config.vm.box_url = "https://dl.dropbox.com/u/2894322/ubuntu-12.04.2-amd64.box"

  config.vm.network :forwarded_port, guest: 1986, host: 1987 # Fanout

  config.vm.provision :chef_solo do |chef|
    chef.json = {}
    chef.add_recipe "fanout::default"
  end
end
