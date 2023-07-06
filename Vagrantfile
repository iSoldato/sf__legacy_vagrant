Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  
  # Проброс порта для доступа к Postgres
  config.vm.network "forwarded_port", guest: 5432, host: 5432

  # Установка Postgres
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y postgresql-8.4
  SHELL
end
