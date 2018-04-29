# 项目说明

---

摘要： 这个小项目跟这[Linux社区推送文章](https://mp.weixin.qq.com/s/dWpwzuxLhiXc7jyH5naxgQ)，学习模拟一个微型区块链，命名为snakeCoin.

## 区块链


> 更通俗的说，它是一个公开的数据库，新的数据存储在被称之为区块block的容器中，并被添加到一个不可变的链chain中（因此被称为区块链blockchain），之前添加的数据也在该链中。对于比特币或其它加密货币来说，这些数据就是一组组交易，不过，也可以是其它任何类型的数据。
>区块链技术带来了全新的、完全数字化的货币，如比特币和莱特币Litecoin，它们并不由任何中心机构管理。这给那些认为当今的银行系统是骗局并将最终走向失败的人带来了自由


### 创世区块

区块链里的第一个区块，索引为0，其前一区块的哈西值为任意数。



### 后继区块

将要添加到区块链中新生成的区块，其索引为区块链中最后一个区块的索引自增1，并需要其数据与其前一区块哈西值结合生成本区块唯一自识别哈西值。



### 产品级区块链

> 要使 SnakeCoin 达到现今的产品级的区块链的高度，我们需要添加更多的功能，如服务器层，以在多台机器上跟踪链的改变，并通过[工作量证明算法（POW）](https://en.bitcoin.it/wiki/Proof_of_work) 来限制给定时间周期内可以添加的区块数量。例如[比特币白皮书](https://bitcoin.org/bitcoin.pdf)。


产品级区块链应该具有分布式、去中心等特性。





## 工作量证明算法

各节点均能保存用户彼此发送 SnakeCoin 的记录的方式，就成为全网公共的、分布式账本：所有的交易信息存储给所有人看，并被存储在该网络的每个节点上。

但是，有个问题：人们从哪里得到 SnakeCoin 呢？现在还没有办法得到，还没有一个称之为 SnakeCoin 这样的东西，因为我们还没有创建和分发任何一个币。要创建新的币，人们需要“挖”一个新的 SnakeCoin 区块。当他们成功地挖到了新区块，就会创建出一个新的 SnakeCoin ，并奖励给挖出该区块的人（矿工）。一旦挖矿的矿工将 SnakeCoin 发送给别人，这个币就流通起来了。

> 不想让挖新的 SnakeCoin 区块太容易，因为这将导致 SnakeCoin 太多了，其价值就变低了；同样，我们也不想让它变得太难，因为如果没有足够的币供每个人使用，它们对于我们来说就太昂贵了。为了控制挖新的 SnakeCoin 区块的难度，我们会实现一个工作量证明[Proof-of-Work](https://en.bitcoin.it/wiki/Proof_of_work)（PoW）算法。工作量证明基本上就是一个生成某个项目比较难，但是容易验证其正确性的算法。这个项目被称之为“证明”，听起来就像是它证明了计算机执行了特定的工作量。


## 共识算法

> 在多节点网络组成的去中心化、分布式公共账本，区块链中。如何才能确保每个节点都有相同的链呢？要做到这一点，我们会使每个节点都广播其（保存的）链的版本，并允许它们接受其它节点的链。然后，每个节点会校验其它节点的链，以便网络中每个节点都能够达成最终的链的共识。这称之为[共识算法consensus algorithm](https://en.wikipedia.org/wiki/Consensus_%28computer_science%29)。



## 运行方式

`python xxx.py`即可，先得安装 `flask` ，建议 `pip` 安装。




## 备注

- vsCode markdown预览：Ctrl+Shift+V