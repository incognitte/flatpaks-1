# flatpaks

A few Flatpaks that I hastly packaged. These are not thoroughly tested so use at your own risk!  
Packaging was adapted mainly from the Flatpaks of Spotify and Flameshot, and Arch Linux's PKGBUILDs.

### Not usable or too buggy

* Android File Tranfer
* Blueman
* QtPass

### How to build

1. Install flatpak-builder
2. Clone the flatpaks repo
```
git clone https://github.com/tinywrkb/flatpaks.git
git submodule init
git submodule update
```
3. Create a working folder for flatpak-builder somewhere
```
mkdir build
```
4. Build the package with flatpak-builder and install it as a user Flatpak app. Replace `manifest.yaml` with the path to application manifest.
```
flatpak-builder --install --user --force-clean --state-dir=build/flatpak-builder --repo=build/flatpak-repo build/flatpak-target manifest.yaml
```
