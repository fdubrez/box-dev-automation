# Script d'install poste de Dev Linux
# https://gist.github.com/tknerr/291b765df23845e56a29
#

Vagrant.configure("2") do |config|
  config.vm.box = "box-cutter/ubuntu1604-desktop"

  provisioner = :ansible

  config.vm.define "ubuntuDev" do |web|
    web.vm.network :private_network, ip: "192.168.33.13"
    web.vm.hostname = "ubuntuDev"
    web.vm.provision provisioner do |ansible|
      ansible.playbook = "playbooks/playbook.yml"
    end
  end

end