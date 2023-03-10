# Task 4 Inery Testnet

## Tutorial to RPC API push transaction

Before you can run your code and call the valued contract function, you need to finish Task 3 in your Account.

To check if you have your CRUD Smart Contract on your account.

```
cline get abi your_inery_account
```

![]()


### Installation

#### Clone the repository

![](https://bashify.io/images/JMHuhc)

```
git clone https://github.com/inery-blockchain/ineryjs.git
```
or

```
git clone https://github.com/diahlaras/ineryjs.git
```

#### Change directory to cloned repository

```
cd ineryjs
```

#### Install NPM packages

![](https://imgur.com/a/pPstUzJ.png)

```
npm install
```

#### Copy .env-sample and rename it to .env

![](https://imgur.com/a/r1NLTQW.png)

```
cp .env-sample .env
```

#### Edit .env file with your information

![](https://imgur.com/a/7tHwnvj.png)

```
your inery account 
your private key
your node url (your ip vps) ex: http://192.168.1.1:8888/
```

### Testing 

Run RPC Example

```
npm run rpc-example
```

if the message like this after running npm run rpc-example, your transaction has been executed on blockchain.

![](https://imgur.com/a/UDUjs2j.png)

### Fixing Error

Thanks to: [alteregogi](https://github.com/alteregogi)

#### Error : Serialization time limit 15000us exceeded:

Change max-transaction-time to more than 15000 in your config.ini
```
nano ./inery-node/inery.setup/master.node/blockchain/config/config.ini
```

#### Error : connect ECONNREFUSED NODE_IP_ADDRESS:8888

Make sure to open your port setting on your VPS provider dashboard and make sure your VPS port **8888** is open, try to check it on [portchecker.co](https://portchecker.co/).

```
sudo ufw allow 8888
```

#### Error: missing create.issuer ( type=name )

You doesn't have Valued Smart Contract on your account, this is on Task 3.
