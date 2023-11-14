# yoctoproject-setup-tools

## Set up a build host environment

### Install the following packages in your host

```bash
sudo apt install docker.io
sudo usermod -aG docker ${USER}
sudo reboot
```

```bash
sudo apt install git
```

## Fetch the source from the git location as below
### Create the working directory where you have plenty of space (>500GB)

```bash
mkdir -p ~/projects/yoctoproject
cd ~/projects/yoctoproject
```

#### (convenient) symlink on host

```bash
sudo ln -sfn ~/projects/yoctoproject /workdir
```

### Download git repo

```bash
mkdir -p /workdir/sources
pushd /workdir/sources
git clone https://github.com/simonsilie/yoctoproject-setup-tools.git
popd

cd /workdir
```

### Start poky build container

```bash
./poky-container.sh 
```
