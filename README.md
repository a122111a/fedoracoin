FedoraCoin 集成/登台树
http://www.fedoracoin.net

版权所有 (c) 2009-2014 比特币开发者

版权所有 (c) 2011-2014 莱特币开发者

版权所有 (c) 2013-2014 FedoraCoin 开发者

什么是 FedoraCoin？
FedoraCoin 是 LiteCoin 的克隆，使用 scrypt 作为工作量证明算法。

RPC端口为22888，P2P端口为44889（testnet为44890）

1分钟出块目标，每10个出块难度调整一次（10分钟难度调整）

总计 500,000,000,000 个硬币。

具有随机块奖励的特殊奖励系统

1 - 100,000: 0 - 5,000,000 FedoraCoin 奖励

100,001 — 200,000：0 - 2,500,000 FedoraCoin 奖励

200,001 — 300,000：0 - 1,250,000 FedoraCoin 奖励

300,001 — 400,000：0 - 625,000 FedoraCoin 奖励

400,001 — 500,000：0 - 312,500 FedoraCoin 奖励

500,001 - 600,000: 0 - 156,250 FedoraCoin 奖励

600,000+ — 10,000 奖励（持平）

如需更多信息，以及可立即使用的 FedoraCoin 客户端软件的二进制版本，请访问http://www.fedoracoin.net。

执照
FedoraCoin 是根据 MIT 许可条款发布的。COPYING有关详细信息，请参阅 参考资料或访问http://opensource.org/licenses/MIT。

开发过程
开发人员在他们自己的树中工作，然后在他们认为他们的功能或错误修复准备就绪时提交拉取请求。

如果它是一个简单/微不足道/无争议的更改，那么 FedoraCoin 开发团队的一名成员就会简单地取消它。

如果它是一个更复杂或可能有争议的更改，那么补丁提交者将被要求在 FedoraCoin IRC 频道（#TIPS on freenode）上开始讨论（如果他们还没有）

如果广泛认为这是一件好事，补丁将被接受。如果代码不符合项目的编码约定（请参阅 参考资料doc/coding.txt）或存在争议，开发人员应该期望返工并重新提交补丁。

该master分支会定期构建和测试，但不保证完全稳定。定期创建标签以指示 FedoraCoin 的新官方稳定版本。

测试
测试和代码审查是开发的瓶颈；我们收到的拉取请求多于我们可以审查和测试的数量。请耐心等待并提供帮助，并记住这是一个对安全至关重要的项目，任何错误都可能使人们付出大量金钱。

自动化测试
强烈鼓励开发人员为新代码编写单元测试，并为旧代码提交新的单元测试。

核心代码的单元测试在src/test/. 编译并运行它们：

cd src; make -f makefile.unix test
GUI 代码的单元测试在src/qt/test/. 编译并运行它们：

qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
make -f Makefile.test
./fedoracoin-qt_test
