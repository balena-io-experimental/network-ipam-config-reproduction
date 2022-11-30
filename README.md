# Network IPAM config reproduction

A test repo to investigate https://github.com/balena-os/balena-supervisor/issues/1576

## Setup
```
balena push $MY_FLEET --source 0 --release-tag app-changed "0" custom-network "0"
balena push $MY_FLEET --source 1 --release-tag app-changed "1" custom-network "1"
```

## Reproduction
Pin to the first release, then pin to the second. Note that one of the services may show as `Downloaded`, which survives Supervisor restarts and device reboots.
