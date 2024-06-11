# Physics Flatpak

Physics is a physical world simulator and playground. You can add squares, circles, triangles, or draw your own shapes, and see them come to life with forces, friction, and inertia.

To know more refer: https://github.com/sugarlabs/physics

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.Physics.git
cd org.sugarlabs.Physics
flatpak -y --user install flathub org.gnome.{Platform,Sdk}//46
flatpak -y --user install org.sugarlabs.BaseApp//24.04
flatpak-builder --user --force-clean --install build org.sugarlabs.Physics.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.Physics
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Physics.json
```