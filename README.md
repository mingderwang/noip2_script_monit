# noip2_script_monit

noip is a script file for noip2 to run under /etc/init.d for start, stop, restart, and status services and work for monit as well.

noip.conf is a monit config file  help for you to keep noip2 running for update dynamic IP for your server running on a non-fixed IP ADSL or dial-up network. In order keep update your new IP to no-ip service server, you need to setup noip2 properly and keep it running. Therefore, we use monit to keep it running correctly, so we need noip script to run as a service.

## Prerequirement
* Monit
* noip2
* Linux (ubuntu)

## Installation
Assume you already install monit, noip2 (from noip.com) on a linux based machine.
If you don't know how to use monit, please check this URL: http://www.tecmint.com/how-to-install-and-setup-monit-linux-process-and-services-monitoring-program/

1. copy noip.conf to /etc/monit/conf.d/
2. copy noip to /etc/init.d
3. reload your monit and make sure noip task is running with "sudo monit summary" command.

## Known Bugs 
1. It could fail on restart sometime. (with a very low chance)

