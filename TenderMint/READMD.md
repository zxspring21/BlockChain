# Tender mint (POS I version)

## Introduction
網路中的驗證人達成共識時，並想要提交這個區塊，交易會透過ABCI送到應用？其ABCI是一個網路套接字協議。
仍夠容忍機器以任何一種危害系統的方式造成故障，稱謂拜占庭容錯(BFT)，其於區塊鍊上的應用關注在p2p網絡和密碼驗證，區塊鍊透過批量方式處理交易，每個區塊包含前一個區塊的加密Hash值，以此來形成一個鍊。

## Tendermint包含兩技術：
區塊鍊共識引擎(Tendermint Core)，保證每台機器以相同的順序紀錄同一筆交易。
通用的應用程式街口，也稱應用程序區塊鍊接口(ABCI)，保證交易可以通過任何一種編程語言，開發者可以利用BFT狀態機複製，其應用可以用任何語言編寫。

### 1. Tendermint compares with other techniques
#### <1>. Comparison with other techniques:
##### -->I.Using 非BFT共識 like Zookeeper, etc, and consul
these application implements a key stored. Zookeeper takes Zookeeper Atomic Broadcast from Paxos. 
etcd and consul used younger and simpler calculation method like Raft which one common group composed from 3-5 machines although it can suffer 1/2 machine has occurred problem. If it happens malfunction, the system might be broken. Each support implementation from other key stored calculation method. They focus on supporting base service in distributed system like dynamic allocation, service discovering, lock, and leader selection.
But Tendermint can suffer 1/3 any format breakdown, inclusive of hack and malicious attack.
##### -->II.blockchain technique, including bitcoin, etherum cryptocurrency, and Hyperledger Burrow distributed ledger design. 

#### <2>. Tender mint which support a effective and safe consensus calculation method can substitute bitcoin or Ethereum traditional currency. 
User must bind sufficient amount of currency to deposit account if they have bad behavior, and their money will be turned back, so it becomes a type of POS calculation method. 
There are some application like ethermint and Cosmos.
#### <3>. Fabric adapted like Tendermint method. It focused on state management, and it required lots of application behavior to operate in docker volume which names chain code. 
It achieved PBFT which invented from IBM to tackle uncertainty in future work by extending Terndermint. 
#### <4>. Burrow takes ethereum virtual machine to implement ethereum transaction mechanism.
And it attaches name registration, permission, natural contract which can substitute with Blockchain API additional characteristic.

### 2. ABCI(Application BlockChain Interface, ABCI)
It uses BFT mechanism by any programming language.
It’s implementation like Tendermint socket protocol(TSP, Teaspoon)

Reference:
http://liuchengxu.org/blog-cn/posts/tendermint/

Tendermint intro:
https://tendermint.com/intro)
