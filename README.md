# ESO Logs Flatpak

Flatpak version of the ESO Logs uploader.

*Note: I haven't yet gotten permission about anything per se (or an answer for taht matter), but I'm putting this as a public git repo. The momenet I get a positive answer I'm going to publish this onto FlatHub*

## How does this flatpak work?

Essentially it decompreses the appimage from the website and repackages it as a flatpak. There is no icon or desktop file present here as they're all present in the appimage itself.

## How to build it 

Inside toolbox container:

```bash
flatpak-builder --user --install --force-clean build-dir com.esologs.Esologs.yml --disable-rofiles-fuse
```

Check for new version:

```bash
flatpak run org.flathub.flatpak-external-data-checker com.esologs.Esologs.yml
```

## How to run it 

```bash
flatpak run com.esologs.Esologs
```