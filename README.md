# Boost Debian Configuration Files

Configuration files to generate a debian package for Boost libraries.

## How to generate a boost library debian package

First, you will need to grab the boost package.  This repository is only configured for a particular version at a time of boost.

```bash
wget https://downloads.sourceforge.net/project/boost/boost/1.70.0/boost_1_70_0.tar.bz2
tar -xjvf boost_1_70_0.tar.bz2
cd boost_1_70_0/
```

Put this debian directory within the boost source directory and call it `debian`

```bash
git clone https://github.com/mikebentley15/boost-deb debian
```

Then build and generate the package.

```bash
./debian/rules build
fakeroot ./debian/rules binary
```

