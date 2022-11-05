Vagrant.configure("2") do |config|

  config.vm.box_download_insecure=true
  config.vm.box = "gusztavvargadr/windows-server-2019-standard"
  config.vm.box_version = "1809.0.2208"
  config.vm.communicator = "winrm"
  
  config.vm.define "iis" do |m|
	   m.vm.network "private_network", ip: "172.17.27.144"
     m.vm.network "forwarded_port", guest: 5985, host: 5985
     m.vm.network "forwarded_port", guest: 5986, host: 5986
  end

  config.vm.provider "virtualbox" do |v|
	   v.memory = 4096
     v.cpus = 4
  end
end
