## ubuntu-1604-nfs-server

Set up NFS server on Ubuntu 16.04.

#### Variables

* `ubuntu_1604_nfs_server_install`: [default: `[]`]: Additional packages to install

* `ubuntu_1604_nfs_server_exports`: Export declarations
* `ubuntu_1604_nfs_server_exports.{n}.path.`:
* `ubuntu_1604_nfs_server_exports.{n}.host.`:
* `ubuntu_1604_nfs_server_exports.{n}.options.`:

#### Examples

##### Simple (share home-directories)

```yaml
---
- hosts: all
  roles:
    - ubuntu-1604-nfs-server
  vars:
    ubuntu_1604_nfs_server_exports:
      - path: /home
        host: myhost
        options: rw,sync,no_root_squash,no_subtree_check
```
