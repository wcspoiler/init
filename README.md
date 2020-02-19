# init
This is a sys admin project repo for School21

Краткий мануал по быстрой настройки виртуалки (без проброса портов - через Host-only Adapter, но пробросы всё равно нужно научиться делать для роджера).

1) VirtualBox -> File -> Host Network Manager...
2) Create (vboxnet0 appears - we've created virtual lan interface between your host and VM).
3) Choose your VM -> Settings -> Network -> Adapter 1 should be NAT, for Adapter 2 choose "Host-only Adapter", Name: vboxnet0).
4) Install Debian like described [here](https://github.com/agavrel/42-Init), except for you should choose enp0s3 network by default during installation for internet connection - for Debian to download and install necessary packages.
5) Now your VM Debian instance will see 2 netwoks: enp0s3 for internet and enp0s8 for netwok (but you can connect to one at a time).

Please note that you should be connected to enp0s8 on your VM Debian to ssh from your mac (host).

Feel free to comment and good luck!


![Screenshot](https://github.com/wcspoiler/init/blob/master/fig.jpg)
