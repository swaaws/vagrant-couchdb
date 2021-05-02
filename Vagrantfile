VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.provider "virtualbox" do |v|
    v.name = "vagrant_couchdb"
  end
  config.vm.box = "generic/ubuntu2004"
  config.vm.network "forwarded_port", guest: 5984, host: 5984
  config.vm.network "public_network"
  config.vm.provision "shell", path: "provision.sh"
  
  config.vm.post_up_message = "-> vagrant ssh -> sudo apt install -y couchdb"
end
