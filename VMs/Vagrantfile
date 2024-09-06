Vagrant.configure("2") do |config|
  config.vm.box = "rockylinux/9"
  config.vm.provider "virtualbox" do |v|
    v.memory = 256
    v.cpus = 1
    v.linked_clone = true
  end
  config.vm.define "controller" do |controller|
    controller.vm.network "private_network", ip: "192.168.10.10"
    controller.vm.hostname = "controller"
  end
  config.vm.define "s1" do |s1|
    s1.vm.network "private_network", ip: "192.168.10.11"
    s1.vm.hostname = "s1"
  end
  config.vm.define "s2" do |s2|
    s2.vm.network "private_network", ip: "192.168.10.12"
    s2.vm.hostname = "s2"
  end
end
