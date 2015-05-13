GoWall 
========

GoWall is a fireall made in GoLang that uses IPTables as it's backbone, the idea is to allow easy and fast configuration of IPTables.

Compilation 
-----------

Compiling it is easy!

### Build it and run it! ####

```bash
$ go build
$ ./main config.json
```

Example Configuration 
---------------

```json
[
    {
        "iface": "eth0",
        "proto": "udp",
        "port": 53,
        "allow": [
            "8.8.8.8",
            "8.8.4.4"
        ]
    }
]
```

This configuration only allows UDP packets to port 53 if from the source IPs "8.8.8.8" and "8.8.4.4".
