# Bodos Raspberry PI

This is the configuration for my raspberry pi.

Steps to install it on your machine:

* Install [NOOBS](https://github.com/procount/noobsconfig/) on the Raspberry Pi
* Select the non ui version of raspbian
* Wait till it is installed and login using `pi` and `raspberry` as password
* Activate ssh as described [here](https://www.raspberrypi.org/documentation/remote-access/ssh/README.md).
* Add your ssh key to the `.ssh/autorized_keys` file on the Raspberry
* Configure your IP in the `hosts` file
* Install ansible with `brew install ansible`
* `sh run.sh`
* Now you have influxdb and grafana installed on the machine
* Open `http://[yourip]:3000` to see the grafana
* Now you can create a username and configure the
  InfluxDB connection. The InfluxDB password
  can be found in the `playbook.yml`

And now you need some data to put into your influxdb to make it
worth it. For example you could build a small air pollution sensor for around
30€ that pushes data into it. Details can be found [here](http://luftdaten.info/).
