# 用java写一个简单的区块链

## 创建区块链

>区块链就是一串或者是一系列区块的集合，类似于链表的概念，每个区块都指向于后面一个区块，然后顺序的连接在一起。那么每个区块中的内容是什么呢？在区块链中的每一个区块都存放了很多很有价值的信息，主要包括三个部分：自己的数字签名，上一个区块的数字签名，还有一切需要加密的数据（这些数据在比特币中就相当于是交易的信息，它是加密货币的本质）。每个数字签名不但证明了自己是特有的一个区块，而且指向了前一个区块的来源，让所有的区块在链条中可以串起来，而数据就是一些特定的信息，你可以按照业务逻辑来保存业务数据。

![区块链示意图](https://github.com/pibigstar/blockchain/raw/master/01.png)

**这里的hash指的就是数字签名**

> 所以每一个区块不仅包含前一个区块的hash值，同时包含自身的一个hash值，自身的hash值是通过之前的hash值和数据data通过hash计算出来的。如果前一个区块的数据一旦被篡改了，那么前一个区块的hash值也会同样发生变化（因为数据也被计算在内），这样也就导致了所有后续的区块中的hash值。所以计算和比对hash值会让我们检查到当前的区块链是否是有效的，也就避免了数据被恶意篡改的可能性，因为篡改数据就会改变hash值并破坏整个区块链。


