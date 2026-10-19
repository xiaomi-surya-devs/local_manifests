Surya Android Building
===========

Getting started
---------------

To get started with Android, you'll need to get familiar with [Source Control Tools](https://source.android.com/setup/develop).

To initialize your local repository using the Google kernel manifest, use a command like this:
```
repo init -u https://github.com/xiaomi-surya-devs/android.git -b lineage-24.0 --git-lfs --depth=1 --no-repo-verify
```
Then use a command like this to clone the local manifest at the root of your local repository:
```
git clone https://github.com/xiaomi-surya-devs/android_local_manifests .repo/local_manifests -b lineage-24.0
```
Then to sync up:
```
repo sync --no-clone-bundle --no-tags -j"$(nproc --all)"
```

Building the ROM
-------------------

Initialize the ROM build environment by sourcing the envsetup.sh script:
```
source build/envsetup.sh
```
Use breakfast to configure the build for your device:
```
breakfast surya userdebug
```
Start the compilation:
```
m bacon
```
