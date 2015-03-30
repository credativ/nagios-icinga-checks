# nagios-icinga-checks

The here listed nagios-icinga-checks were created during my work for credativ GmbH.

## What to do with the checks
The usage of the checks depends on what kind of checks they are:
* nrpe plugins must be copied to the monitoring client
* normal checks must be run on the monitoring server

## How to use check_openvpn
The plugin is a normal check which must be run on the monitoring server. It queries the target OpenVPN server and outputs OK, etc.
```
$ python check_openvpn --help
usage: check_openvpn [-h] [-p PORT] [-t] host

positional arguments:
  host                  the OpenVPN host name or ip

optional arguments:
  -h, --help            show this help message and exit
  -p PORT, --port PORT  set port number
  -t, --tcp             use tcp instead of udp
```

## How to use check_puppetagent
The plugin is an NRPE check and needs to be run on the monitoring client, thus the client which Puppetagent needs to be monitored.
```
$ python check_puppetagent --help
usage: check_puppetagent [-h] [-w WARN] [-c CRIT]

optional arguments:
  -h, --help            show this help message and exit
  -w WARN, --warn WARN  seconds after last Puppet run which issues a warning
  -c CRIT, --crit CRIT  seconds after last Puppet run which are critica
  ```
  -c CRIT, --crit CRIT  seconds after last Puppet run which are critica  
```
