Vagrant.configure("2") do |config|
    config.vm.box = "hashicorp/precise32"
    config.vm.define :web do |web_config|
        web_config.vm.network "private_network", ip: "192.168.50.10"
        #novo
        web_config.vm.provision "shell", inline: <<-SHELL
		sudo rpm -ivh http://yum.puppetlabs.com/puppetlabs-release-el-7.noarch.rpm
              sudo yum install -y puppet
        SHELL
    end
end
