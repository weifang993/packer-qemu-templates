# Ubuntu packer templates

## Create vagrant image for use with vagrant libvirt

```bash
packer build -var-file=ubuntu1604.json ubuntu-vagrant.json
```

## Create qcow2 image for use with kvm

```bash
packer build -var-file=ubuntu1804.json ubuntu-wei.json
```
The image format is: qcow2. To get info on the image:

* `qemu-img info ubuntu1804`

### Known Issues ###

Tried to use "disk_additional_size": ["10G"] and build failed.