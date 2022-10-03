# MQTTPi

Simple setup for for a mosquitto broker and node-red, for testing and home use.


## Raspberry Pi Imager

Get the Raspberry Pi Imager from https://www.raspberrypi.com/software/ (lets you set up a lot of stuff before even writing the OS to the SD card).

![](imgs/Raspberry%20Pi%20Imager%20v1.7.2.png)

### Options to set

* Operating system > Raspberry Pi OS (Other) > Raspberry Pi OS Lite 32bit
* Cogwheel button > Enable SSH and set all the rest how you like it.

Write it to the SD card

Put the SD card into your RasPi and boot it, since newer releases RasPi OS take quite a while on it's first boot.

## Connect to your RasPi

Connect to your RasPi over SSH. 

Or connect it to a screen and a keyboard.

## Installing Prerequisites

Install git, ansible and python3-docker

```
sudo apt install ansible git python3-docker
```

Then you can get the geerlingguy.docker_arm ansible role to set up docker

```
ansible-galaxy install geerlingguy.docker_arm
```

And get the playbook with 

```
git clone https://github.com/morgulbrut/MQTTPi.git
```

Change to the directory with 

```
cd MQTTPi
```

Finally run the playbook with 

```
ansible-playbook -v mqttpi.yml
```

