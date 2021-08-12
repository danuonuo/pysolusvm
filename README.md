# pySolusVM

Python Module to interact with SolusVM API

Tested with SolusVM v1.23.xx

# Install

```bash
$ pip3 install git+https://github.com/danuonuo/pysolusvm
```

You'll need a SolusVM API ID and Key. You can create one in SolusVM under Configuration > API Users > Create API User.

# Example Usage

```
from pysolusvm import SolusVM

solus = SolusVM('solusvm.example.com', 'API-ID', 'API-KEY')

nodes = solus.listNodesById()
virtualservers = []
for node in nodes['nodes'].split(','):
        virtualservers.extend(solus.listVirtualServers(node))
```
