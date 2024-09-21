---
title: "Win10"
date: 2024-09-21T13:22:51Z
image: 'static/image/win10.jpg'
---

# Your install windows in google cloud now

```
sudo apt update
```

```
sudo apt install qemu-kvm apache2 ufw p7zip-full -y 
```

# Allow your ufw "VNC' now

```
sudo ufw allow 'VNC'
sudo ufw status
```

# Download file now

```
wget -O RTL8139F.iso 'https://drive.google.com/uc?export=download&id=1wDL8vo9mmYKw1HKXZzaYHoKmzSt_wXai'
wget -O 10.7z 'https://archive.org/download/windows-10.7z_20240424/Windows%2010.7z'
```

# install novnc now and use

```
sudo apt install novnc -y
sudo /usr/share/novnc/utils/launch.sh --listen 8080 --vnc localhost:5900
```

# run qemu system-x86_64 now

```
sudo qemu-system-x86_64 -M q35 -cpu core2duo,+avx -smp sockets=1,cores=4,threads=2 -m 8G -drive file=10.qcow2,aio=threads,if=virtio,cache=unsafe -vga none -device virtio-gpu-pci -device intel-hda -device hda-duplex -device virtio-net-pci,netdev=n0 -netdev user,id=n0 -accel tcg,thread=multi,tb-size=2048 -device virtio-balloon-pci -device virtio-serial-pci -device virtio-rng-pci -device intel-iommu -vnc :0 -cdrom RTL8139F.iso
```


