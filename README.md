This container allows to export a single share via NFS4.
The nfs server listens on tcp/2049.

USAGE:

```
docker run -d --privileged \
	-v /home:/export \
	-e "ALLOWED_CLIENTS=*" \
	evermind/nfs4-server
```

Everything that is mounted to /export on the container will be exported to all clients in ALLOWED_CLIENTS (separate multiple clients by whitespace).


Derived from https://github.com/sjiveson/nfs-server-alpine and stripped down to the absolute minimum.
