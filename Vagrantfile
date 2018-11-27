Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.define "vagrant1" do |vagrant1|
    vagrant1.vm.box = "centos/7"
    vagrant1.vm.network "forwarded_port", guest: 80, host: 8080
    vagrant1.vm.network "forwarded_port", guest: 443, host: 8443
    vagrant1.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", disabled: true
    vagrant1.vm.network :forwarded_port, guest: 22, host: 2221, auto_correct: true
    vagrant1.ssh.port = 2221
  end
  config.vm.define "vagrant2" do |vagrant2|
    vagrant2.vm.box = "centos/7"
    vagrant2.vm.network "forwarded_port", guest: 80, host: 8081
    vagrant2.vm.network "forwarded_port", guest: 443, host: 8444
  end
  config.vm.define "vagrant3" do |vagrant3|
    vagrant3.vm.box = "centos/7"
    vagrant3.vm.network "forwarded_port", guest: 80, host: 8082
    vagrant3.vm.network "forwarded_port", guest: 443, host: 8445
    vagrant3.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", disabled: true
    vagrant3.vm.network :forwarded_port, guest: 22, host: 2223, auto_correct: true
    vagrant3.ssh.port = 2223
  end
  config.vm.define "vagrant4" do |vagrant4|
    vagrant4.vm.box = "centos/7"
    vagrant4.vm.network "forwarded_port", guest: 80, host: 8083
    vagrant4.vm.network "forwarded_port", guest: 443, host: 8446
    vagrant4.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", disabled: true
    vagrant4.vm.network :forwarded_port, guest: 22, host: 2224, auto_correct: true
    vagrant4.ssh.port = 2224
  end
end