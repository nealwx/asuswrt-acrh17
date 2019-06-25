The GPL source is created for ASUS wireless router related products. Please visit the ASUS support site (http://support.asus.com) to get the latest GPL tarball.It has a lot in common with many wireless router open source projects, including Oleg/Tomato/DD-WRT/OpenWRT. Thanks the developers of those projects for making the source code available.

Set Up Environment(Ubuntu 16.04/14.04)

	1. prepare environment

		sudo apt-get update
sudo apt-get install libtool-bin cmake libproxy-dev uuid-dev liblzo2-dev autoconf automake bash bison \
bzip2 diffutils file flex m4 g++ gawk groff-base libncurses-dev libtool libslang2 make patch perl pkg-config shtool \
subversion tar texinfo zlib1g zlib1g-dev git-core gettext libexpat1-dev libssl-dev cvs gperf unzip \
python libxml-parser-perl gcc-multilib gconf-editor libxml2-dev g++-multilib gitk libncurses5 mtd-utils \
libncurses5-dev libvorbis-dev git autopoint autogen sed build-essential intltool libelf1:i386 libglib2.0-dev \
xutils-dev lib32z1-dev lib32stdc++6 xsltproc gtk-doc-tools

sudo apt-get install lib32z1-dev lib32stdc++6

	2. setup development system

	Qualcomm IPQ806x/IPQ40xx ARM SoC models
	===============================

		For example, BRT-AC828.

		To install the tools:
		    - extract tools/openwrt-gcc463.arm.tar.bz2 directory to /opt
		    - add /opt/openwrt-gcc463.arm/bin to your path
			export PATH=$PATH:/opt/openwrt-gcc463.arm/bin

		    - If you want to build small utilities out of asuswrt box,
		      add STAGING_DIR environment variable as below:
	
		      export STAGING_DIR=/opt/openwrt-gcc463.arm

	Note: Broadcom/Ralink(except 4708 series) platform use the same toolchain for user space program, so please set PATH to the same directory as above

   3. build firmware.
	
	a. rt-ac82u
		cd release/src-qca-dakota
		make rt-ac82u


	note: RT-ACRH17 belong to RT-AC82U serious
