# Persistent SSH Tunnel Service
This repository holds files related to a custom systemd service, which establishes arbitrary ssh tunnels and persists them while the service is running.

To install, copy all files from this repository except READMEs to their respective directories, matching project root to filesystem root (`/`).

File `ssh-tunnel@.service` is a [service template](https://fedoramagazine.org/systemd-template-unit-files/). After specifying a host in `/etc/ssh-tunnel.conf`, for example `example.com-1234`, launch service using `service ssh-tunnel@example.com-1234 start` or enable it at startup using `service ssh-tunnel@example.com-1234 enable`.

Config file `/etc/ssh-tunnel.conf` is written as a normal [SSH config file](https://linux.die.net/man/5/ssh_config).