VAGRANTFILE_API_VERSION = "2"

Vagrant.require_version ">= 2.0.2"
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"

  # Disable the new default behavior introduced in Vagrant 1.7, to
  # ensure that all Vagrant machines will use the same SSH key pair.
  # See https://github.com/mitchellh/vagrant/issues/5005
  config.vm.provider :virtualbox do |vb|
    vb.memory = 4096
    vb.cpus = 2
  end
  config.vm.provision "shell", path: "setupdocker.sh"

end
