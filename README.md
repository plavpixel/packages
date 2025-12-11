Void packages repo maintained by the unofficial Void Linux Community.

Packages added by [plavpixel](https://github.com/plavpixel/) in this repo fork:
- legcord
- limine-entry-tool
- linux-cachyos (unfinished)
- svc

Each package is its own branch, everyone is encouraged to review my templates and open issues/PRs fixing them.

You can use this repo in two ways, either localy or remotely.

## Local install

### Clone the repository anywhere

```sh
git clone https://github.com/voiders-community/packages ~/ports --shallow-submodules --recursive --depth=1
```

### Add the repository

```sh
echo "repository=$HOME/ports/hostdir/binpkgs" | sudo tee /etc/xbps.d/10-voiders-community-local-repo.conf
```

### Sync the repos

```sh
sudo xbps-install -S
```

## Remote install

### Add the repository

```sh
echo "repository=https://github.com/voiders-community/packages/raw/refs/heads/master/hostdir/binpkgs/" | sudo tee /etc/xbps.d/10-voiders-community-local-repo.conf
```

### Sync the repos

```sh
sudo xbps-install -S
```


## How to add a new package

Write your template in ./srcpkgs/YOUR_PACKAGE/template like you'd do with the official repo, then run `./make build YOUR_PACKAGE`, if you've installed the repo using the local install you can now do `xbps-install -S YOUR_PACKAGE`.

## How to push my new package

To add a new package you just need to open a PR with your srcpkgs (DO NOT push any .xbps files)
