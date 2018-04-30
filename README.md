# Instantcoin ( BTI )
----------------------

RPC Port = 7331

P2P Port = 17331

addnode=bti1.instant.industries

# Installing Windows Subsystem for Linux With Windows 10, Microsoft has released a new feature named the Windows Subsystem for Linux (WSL). This feature allows you to run a bash shell directly on Windows in an Ubuntu-based environment. Within this environment you can cross compile for Windows without the need for a separate Linux VM or server. Note that while WSL can be installed with other Linux variants, such as OpenSUSE, the following instructions have only been tested with Ubuntu.

# This feature is not supported in versions of Windows prior to Windows 10 or on Windows Server SKUs. In addition, it is available only for 64-bit versions of Windows.

# Full instructions to install WSL are available on the above link. To install WSL on Windows 10 with Fall Creators Update installed (version >= 16215.0) do the following:

# Enable the Windows Subsystem for Linux feature Open the Windows Features dialog (OptionalFeatures.exe) Enable 'Windows Subsystem for Linux' Click 'OK' and restart if necessary Install Ubuntu Open Microsoft Store and search for Ubuntu or use this link Click Install Complete Installation Open a cmd prompt and type "Ubuntu" Create a new UNIX user account (this is a separate account from your Windows account) After the bash shell is active, you can follow the instructions below, starting with the "Cross-compilation" section. Compiling the 64-bit version is recommended but it is possible to compile the 32-bit version.

# WSL BUILD INSTRUCTIONS 

git clone https://github.com/Liskcoin/bitcoin-instant 

cd bitcoin-instant

sudo apt-get install build-essential

sudo apt-get install libtool autotools-dev autoconf libssl-dev

sudo apt-get install libboost-all-dev

sudo add-apt-repository ppa:bitcoin/bitcoin

sudo apt-get update

sudo apt-get install libdb4.8-dev

sudo apt-get install libdb4.8++-dev

sudo apt-get install libminiupnpc-dev

sudo apt-get install libqt4-dev libprotobuf-dev protobuf-compiler

sudo apt-get install libqrencode-dev

./autogen.sh

./configure

make clean

make

# add -y if you get "Abort." error.

# To use WSL build with gui , an Xserver will need to be installed on the Windows 10 system and the DISPLAY variable will need to be set in Bash. >> install: VcXsrv & PuTTY. >> launch: Xlaunch(VcXsrv) >> open up WSL console then type : 


export DISPLAY=:0

cd bitcoin-instant

cd ./src/qt/

./instantcoin-qt

# still need help? *join Bitcoin-instant telegram : https://t.me/bitcoin_instant


