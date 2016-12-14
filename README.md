Manifest CypherOS For Glaxy Grand Prime
=======================================

Instructions
---------------

To get started with CyanogenMod, you'll need to get familiar with
[Git and Repo](http://source.android.com/download/using-repo).

Initializing:

First, create a folder to hold the source code: 

	mkdir ~/aoscp

Next, naviate into that new directory via the terminal:

	cd ~/aoscp

To initialize your local repository, use this command:

	repo init -u https://github.com/CypherOS/platform_manifest.git -b n7.1

Also add the local manifests:

	git clone https://github.com/Cyanogenmod-G530H/local_manifest -b n7.1 .repo/local_manifests

Then sync up with this command:

	repo sync -fcj4 --force-sync
	
You can make the 4 higher depending on how fast your internet connection is. 

-------------
 
_Building from source_
---------------

First:

	cd ~/aoscp
	
Second:

	$ echo "export USE_CCACHE=1" >> ~/.bashrc
	$ ~/aoscp/prebuilts/misc/linux-x86/ccache/ccache -M 50G

Third:

	. build/envsetup.sh
	brunch fortuna3g or brunch fortunave3g
