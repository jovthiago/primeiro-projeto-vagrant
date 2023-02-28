Vagrant.configure("2") do |config|
  
  config.vm.box_download_insecure=true
  config.vm.define "nginx"
  config.vm.box = "ubuntu/focal64"
  config.vm.network "forwarded_port", guest: 80, host: 8090
  config.vm.network "public_network", ip: "192.168.5.112"
  config.vm.provision "shell", path: "script.sh"
  config.vm.synced_folder "site/", "/var/www/html"
    
  #configuração da maquina
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end


end