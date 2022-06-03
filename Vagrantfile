Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-10.04"
  config.vm.provision "shell", privileged: false, inline: <<-SHELL
    sudo sed -i 's/us.archive/old-releases/g' /etc/apt/sources.list
    sudo sed -i 's/security.ubuntu/old-releases.ubuntu/g' /etc/apt/sources.list
    sudo apt-get -y update
    sudo apt-get install -y postgresql-8.4 postgresql-client-8.4
    SHELL
end
