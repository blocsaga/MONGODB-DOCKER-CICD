Vagrant.configure("2") do |config|
    config.name = "for_mongodb"
    config.vm.box = "bento/ubuntu-22.04"
    config.vm.network "forwarded_port", guest: 80, host: 8080

    config.vm.provider "virtualbox" do |vb|
        vb.gui = false
        vb.memory = "1024"
        vb.cpus = 2
    end
    config.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y nginx
    SHELL

end

    