Vagrant.configure(2) do |config|
  config.vm.box = "bento/debian-8.4"

  config.ssh.forward_agent = true
  config.ssh.forward_x11 = true

  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    # vb.gui = true
  end

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y xorg virt-manager ssh-askpass
  SHELL
end
