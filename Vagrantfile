# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.define "acs" do |acs|
    acs.vm.box = "centos/7"
    acs.vm.hostname = "acs"
	acs.vm.synced_folder ".", "/vagrant", type: "nfs"
    acs.vm.network "private_network", ip: "192.168.33.50"
  end

  config.vm.define "collectd" do |collectd|
    collectd.vm.box="bento/centos-5.11"
    collectd.vm.hostname = "collectd"
	collectd.vm.synced_folder ".", "/vagrant", type: "nfs"
    collectd.vm.network "private_network", ip: "192.168.33.60"
  end

  config.vm.define "logstash" do |logstash|
    logstash.vm.box = "centos/7"
    logstash.vm.hostname = "logstash"
	logstash.vm.synced_folder ".", "/vagrant", type: "nfs"
    logstash.vm.network "private_network", ip: "192.168.33.70"
  end

end