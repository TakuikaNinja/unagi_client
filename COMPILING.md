# Anago CLI compilation on Arch Linux

Dependencies: `squirrel libusb wxwidgets-gtk3`

```bash
mkdir Anago0.6.2
cd Anago0.6.2
git clone https://github.com/sharkpp/unagi_kazzo.git
git clone https://github.com/TakuikaNinja/unagi_client.git
mv unagi_kazzo/ kazzo
cd unagi_client
mkdir SQUIRREL2 && cd SQUIRREL2
ln -s /usr/include/ include
ln -s /usr/lib/ lib
cd ../anago
make -f Makefile.unix
```

For Debian-based systems, the dependencies are `libsquirrel-dev libusb-dev libwxgtk3.2-dev`

Due to packaging differences, the "include" symlink and anago.mk `-I/-l` flags must be changed to reference Squirrel's includes directory and version number.

