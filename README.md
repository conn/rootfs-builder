# Rootfs Builder
A script that builds a Debian rootfs with configurations

## Setup:
Some dependencies:
* ansible
* debootstrap
* docker
* jq
* xz-utils

My image-builder role should cover all dependencies needed to run my
scripts/templates.

You'll also need to pull down the roles specified in the requirements file:
```
cd ansible/roles/ && ansible-galaxy install -r requirements.yml -p .
```
If you want to bake in a custom public key, you can put it in the `keys`
directory and reference it in `variables.json`.

You can also twiddle the version in `variables.json`.

## Usage:
Run the build:
```
./rootfs-builder
```
