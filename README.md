# 

# NFS Mounting via Execution Node and Execution Environment

## Execution Node
- install nfs-utils, rpcbind
- mount command: 
`mount -t nfs 192.168.56.12:/mnt/nfs_shares/docs -o rw,context="system_u:object_r:container_file_t:s0" /ansible --make-shared`

- change AAP 'Job Settings' to allow directories:

Paths to expose to isolated jobs
```json
	[	
	  "/ansible:/ansible:rw",
	  "/etc/pki/ca-trust:/etc/pki/ca-trust:O",
	  "/usr/share/pki:/usr/share/pki:O"
	]		
```
