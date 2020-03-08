# Build-Instance

*This branch contains the necessary changes for building unofficial
CentOS Vagrant images with the VirtualBox Guest Additions, using Packer.
The intention is to follow the official kickstart files as close as
possible; using a branch allows easy merging from the upstream repo.*

This git repo contains kickstart files that define how the various CentOS Cloud Instances are built. These kickstarts are parsed with `virt-install`. Every kickstart must be named in the following convention:

```
CentOS-<release ver>-<arch>-<target>-<tag>.ks
```

eg:

```
CentOS-6-x86_64-OpenStack-6.5_20140119.ks
```

Along with every kickstart is a metadata file, with the same name as the kickstart, except ending with .json ( because they are json files )

# Git Tags:

As a part of the instance release process, the content used to build that instance MUST be tag'd away 

# Notes:

*  ReleaseVer must always only be 5 or 6 or 7, never the point release ( but you can overload the TAG component in the name with anything, I like using the point release there, along with the datestamp ).

# ToDo:

* Provide some example kickstarts
* Provide some example metadata json's
* Import the virt-install wrapper bash script
