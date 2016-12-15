# Packer Linux template for Vagrant


This example build configuration installs and configures Linux such as CentOS,... minimal using Packer, and then generates two Vagrant box files, for:

  - VirtualBox

The example can be modified to use more provision to fully configure (or partially) configure a box file suitable for deployment for development environments.

## Requirements

The following software must be installed/present on your local machine before you can use Packer to build the Vagrant box file:

  - [Packer](http://www.packer.io/)
  - [Vagrant](http://vagrantup.com/)
  - [VirtualBox](https://www.virtualbox.org/) (if you want to build the VirtualBox box)

## Usage

Make sure all the required software (listed above) is installed, then cd to the directory containing this README.md file, and run:

    $ packer build centos6-8.json

After a few minutes, Packer should tell you the box was generated successfully.

## Testing built boxes

There's an included Vagrantfile that allows quick testing of the built Vagrant boxes. From this same directory, run one of the following commands after building the boxes:

    $ vagrant up virtualbox --provider=virtualbox

## Author Information

Created in 2016 by [Sida Say](https://www.davijournal.com/).
