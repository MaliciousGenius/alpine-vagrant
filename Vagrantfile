Vagrant.configure("2") do |config|

  config.vm.define "gui" do |gui|
    gui.vm.hostname = "control-panel.home.local"
    gui.vm.box = "centos/7"
    gui.vm.box_check_update = false

    gui.vm.network "public_network", ip: "172.16.0.252", netmask: "255.255.0.0", bridge: "en0: Wi-Fi (AirPort)"

    gui.vm.provision :ansible do |ansible|
      ansible.playbook = "provision.yml"
    gui

    gui.vm.provider "virtualbox" do |vm|
      vm.cpus = "1"
      vm.memory = "256"
      vm.gui = true
    end
  end
end