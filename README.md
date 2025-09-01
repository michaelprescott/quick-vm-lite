# Quick VM Lite

Bash scripts to quickly setup virtual machines when containers are not enough. "quickly" means setup and teardowns in seconds if RAM flag is used.

## Prerequisites

* Platform(s)
    * macOS - Thoroughly tested on Intel and Apple Silicon systems running the latest macOS.  If you'd like to run the same on Windows PCs, try installing Windows System for Linux (WSL).

* VMWare Fusion

* Tools for working with ISO images
    * brew install cdrtools
    * brew install xorriso

* Tools for extracting ISO images and other archive files
    * https://www.7-zip.org/download.html
        -> https://www.7-zip.org/a/7z2501-mac.tar.xz

```
# Install 7-zip and make accessible to CLI tools and scripts

VERSION=7z2501 # Revise VERSION var to match the downloaded version
echo $PATH | grep -o /usr/local/bin # Verify /usr/local/bin is in the path
mkdir -p $HOME/Developer/Tools/7z/bin   # Prepare to save 7z in $HOME/Developer/Tools/7z/bin
curl -o $HOME/Developer/Tools/7z/${VERSION}-mac.tar.xz https://www.7-zip.org/a/${VERSION}-mac.tar.xz # Download 7z
tar xvf $HOME/Developer/Tools/7z/${VERSION}-mac.tar.xz -C $HOME/Developer/Tools/7z/bin # Extract 7z
ln -s $HOME/Developer/Tools/7z/bin/7zz /usr/local/bin/7zz # Create a symlink to 7zz in /usr/local/bin
7zz --help # Verify it is extracted and available to CLI environment
```
