#Sample configuration:

regtest=1
rpcport=83232
rpcconnect=127.0.0.1
rpcuser=xxx
rpcpassword=yyy

#Start
```shell
$ ./zcash-fetch-params --regtest
$ ./zcash-init
$ ./zcashd --regtest
```
#Transaction and CLI
```shell
#Get info
$ ./zcash-cli getinfo
#Generating a t-addr
##List existing account
$ ./zcash-cli getaddressesbyaccount ""
##Generate
$ ./zcash-cli getnewaddress

#Generate a z-addr
$ ./zcash-cli z_getnewaddress

##List existing z-addrs
$ ./zcash-cli z_listaddresses

#Create coinbase notes for t-addr
$ ./zcash-cli generate 201

#Sweep up coinbase UTXOs from a transparent address
$ ./zcash-cli z_shieldcoinbase tMyMiningAddress zMyPrivateAddress

#Sending coins with your z-addr
$ ./zcash-cli z_sendmany "$SENDER" "[{\"amount\": 0.8, \"address\": \"$RECEIVER\"}]"
```
