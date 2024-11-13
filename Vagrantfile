# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "debian/bookworm64"
  config.ssh.insert_key = false
  config.vm.define "web1" do |web1|
    web1.vm.hostname = "web1"
    web1.vm.network "forwarded_port", guest:80, host: 8080
    web1.vm.network "forwarded_port", guest:443, host: 4433
  end
end