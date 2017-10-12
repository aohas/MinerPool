cpuminer-win64
==============

cpuminer can be run either in pool or solo mode. When running in solo mode an entire block must be found before any MaxCoins will be earnt - this is unlikely to happen due to the quantity of miners on the network. Running in pool mode allows you to receive a portion of the coins earned proportional to the amount of work you contributed, as determined by the hashpower you provide.

To use cpuminer in solo mode use the following command:

minerd.exe -a keccak -o 127.0.0.1:8669 -u RPCUSER -p RPCPASSWORD

The IP address and port are the address/port of the machine your wallet is running on. The RPC credentials are configured in your maxcoin.conf file.

To use cpuminer in pool mode use the following command:

minerd.exe -a keccak -o stratum+tcp://POOLURL:3333 -u USERNAME.WORKERNAME -p WORKERPASSWORD

The mining pool URL, username and password are determined by the mining pool you pick. You must sign up for a pool, create a work and configure the command based upon these details. A list of pools can be found at www.maxcoin.co.uk/pools.

For ease of use, copy the following into a .bat file:

@echo off
minerd.exe -a keccak -o stratum+tcp://POOLURL:3333 -u USERNAME.WORKERNAME -p WORKERPASSWORD