## File List
Things that are here:

- virt-addr -- list the ip addresses assigned to a domain by scanning
  the lease file for the `default` libvirt network.
- virt-disks -- list the disk images associated with a domain.
- virt-delete -- delete a domain and the disks images it was using.
- virt-from -- create a new domain from a snapshot of an existing
  image.
- virt-hosts -- return an `/etc/hosts` style listing of running
  domains and their ip addresses.
- virt-interfaces -- produce a listing of network interfaces
  associated with a domain.
- virt-pick -- use xdialog to select a domain.  Accepts the same
  arguments as "virsh list".
- virt-vol -- quickly create a snapshot from an existing libvirt
  volume
- create-config-drive -- create a cloud-init/openstack compatible
  config ISO image
- virt-boot -- wrapper for virt-install to create a snapshot,
  populate a cloud-init compatible config drive, and boot an instance.

## Usage

- To create the config iso, run this:
  ./create-config-drive --ssh-key /root/.ssh/id_rsa.pub --user-data ./user-data --hostname <hostname> config.iso

- The config.iso can be reused if you remove the cdrom from domain definition. 

- default cloud-init user names

```
## Admin username:
##    Ubuntu: ubuntu
##    Debian: debian
##    Fedora: fedora
##    CentOS: centos
##    CoreOS: core
##    RHEL: cloud-user
```
