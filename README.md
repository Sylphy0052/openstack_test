# openstack_test
For study openstack


## OpenStackの役割

![openstack](./src/499901.png)

## 仮想マシンインスタンスの起動
- [参考:Nested KVM環境でのNewton版OpenStack構築メモ](https://qiita.com/ttsubo/items/8eeb047c2a87d605a6ef)
### Novaを使う

- `sudo virt-install --name newton --ram 8192 --disk path=/home/pyente/iso/newton.qcow2,size=80,bus=virtio,format=qcow2 --vcpus 4 --os-variant rhel7 --network bridge=virbr0 --graphics none --console pty,target_type=serial --location /home/pyente/iso/CentOS-7-x86_64-Minimal-1611.iso --extra-args 'console=ttyS0,115200n8 serial'`

- `ERROR    Host does not support any virtualization options` -> `sudo apt-get install -y qemu-kvm`で解決

-
