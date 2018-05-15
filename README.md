# docker-elasticsearch

## macOS with Docker for Mac

The vm.max_map_count setting must be set within the xhyve virtual machine:

```
$ screen ~/Library/Containers/com.docker.docker/Data/com.docker.driver.amd64-linux/tty
```

Log in with root and no password. Then configure the sysctl setting as you would for Linux:

```
sysctl -w vm.max_map_count=262144
```

To set this value permanently, update the `vm.max_map_count` setting in `/etc/sysctl.conf`.

Ensure the Docker.app has enough RAM for the VM, check the Advanced settings for that.
