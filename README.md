# Munin Server

[![Docker Stars](https://img.shields.io/docker/stars/jekil/docker-munin-server.svg)](https://hub.docker.com/r/jekil/docker-munin-server/)
[![Docker Pulls](https://img.shields.io/docker/pulls/jekil/docker-munin-server.svg)](https://hub.docker.com/r/jekil/docker-munin-server/)
[![Twitter Follow](https://img.shields.io/twitter/follow/jekil.svg?style=social)](https://twitter.com/jekil)

This image provides a munin server, configured as CGI, using nginx.
It can be totally configured by command line, passing the hosts you want to monitor as argument.

## Quick Start

Use the following command to start the munin server, in the NODES argument you should supply a space separated list of `<name>:<host>` munin node pairs. (i.e. `foo.local:127.0.0.1 bar.remote:1.2.3.4`)

    docker run -p 80 -e NODES="foo.local:127.0.0.1 bar.remote:1.2.3.4" --name munin-srv -d jekil/docker-munin-server

## Technical details

Ports exposed:

* 80

Environment Variables :

* `NODES`: Space separated list of `<name>:<host>` munin node pairs. (i.e. `foo.local:127.0.0.1 bar.remote:1.2.3.4`)

Volumes:

* /var/lib/munin
* /var/log/munin
* /etc/munin
