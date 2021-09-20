# btcusdt
比特币自动交易程序，欧易API接口

btcusdt.exe 和 set_api.exe是Windows系统使用的；
btcusdt.py和set_api.py是界面版的Python程序，可以运行在任何桌面操作系统，只要安装有Python环境；
mark.py和start.py是命令行版Python程序，可以运行在CentOS等命令行操作系统，使用说明请见：
https://www.btcusdt.org/d/1

BTCUSDT量化交易云是一个开源项目，官方网站：
www.btcusdt.org

## 执行体下载地址
[Windows版本量化交易执行体](http://img.btcusdt.org/tool/btcusdt_win.zip)

[Python源代码（命令行版）](http://img.btcusdt.org/tool/btcusdt_python.zip)

[Python源代码（界面版）](http://img.btcusdt.org/tool/btcusdt_python_ui.zip)

[量化交易执行体使用说明](https://www.btcusdt.org/d/522)

```
支持本站发展，如果您是第一次注册欧易交易所，请使用下面的邀请链接注册：
https://www.ouyi.fit/join/8878217
或者在注册的时候输入邀请码：8878217
```
```
赞助本站：
BTC赞助地址：1PDqGEvr6kRLv66Z6PqUK4ncxvfdUTEhz1
USDT赞助地址：1PDqGEvr6kRLv66Z6PqUK4ncxvfdUTEhz1
ETH赞助地址：0x9ecee129c83f49f7e0c58b61138f05d906de7746
```
- Windows版本为界面版，下载后首先通过set_api配置交易所API，然后再运行btcusdt程序开始自动交易即可；
- Python源代码命令行版可运行在任意操作系统上，只要安装并配置好Python环境即可，推荐使用Python3.7.7版本，需要安装requests库，通过手动修改`okex_api.json`文件配置交易所API，在CentOS下通过以下命令可以使执行体在后台自动执行：
```
nohup python3 start.py &
```
通过以下命令终止进程，停止交易：
```
ps -aux | grep start.py
kill -9 获取到的进程号
```
- Python源代码界面版可运行在任意桌面版的操作系统上，只要安装并配置好Python环境即可，推荐使用Python3.7.7版本，需要安装requests库，使用方法与Windows版本为界面版类似；

### API注意事项：

- 如果你不是运行在固定IP的云主机上的话，请不要设置绑定IP，否则无法使用；
- 为了你的账号安全申请API时，请勾选只读和交易权限，请勿勾选提现权限；
- `okex_api.json`中的flag为交易盘选项，0为真实盘，1为模拟盘；

### 常见问题
##### 开始交易后卡住不动

- API设置不正确，请检查API是否配置正确，真实盘和模拟盘的API是不同的，需要分别设置；
- 国内网络无法访问交易所，请使用境外云主机运行执行体，推荐使用香港云主机；
- 请勿在国内使用翻墙软件开启执行体，由于兼容性的问题，使用翻墙软件很大概率会无法运行；
- 可以使用腾讯云或AWS的香港云主机，根据你的自身情况选择Windows操作系统或CentOS操作系统均可；

## 什么是量化交易执行体？
量化交易执行体是能够自动执行本项目云端运算结果，实现自动交易的程序，该执行体自身不具备任何交易策略，由云端数十台高性能服务器对全球海量数据结合人工智能、机器学习进行大数据建模分析，并将分析的结果实时同步给执行体，由执行体进行具体的交易执行。

## 执行体和自动交易机器人有什么区别？
自动交易机器人是采用交易策略进行自动交易的程序，其计算能力来源于运行机器人程序的计算机，所以只能进行简单的交易策略执行，本社区的量化交易执行体自身不进行任何的交易策略计算，完全依托于云端的运算结果，云端由数十台，将来会扩容到上百台高性能服务器组成，对各种技术指标、全球交易数据、新闻舆情等进行综合分析，其分析能力是自动交易机器人远远无法比拟的，本量化交易云采用算力集中、执行分布的系统架构，大大的提高了交易的准确性，同时实现了效率的最大化。

## 量化交易执行体收费么？
本项目为开放项目，量化交易执行体程序完全开放，任何人都可以随意下载使用，不收取任何费用。

## 量化交易执行体如何保证资金安全？
量化交易执行体是一个交易执行程序，只是向交易所提交下单的指令，用户的资金并不经过执行体，由用户自己申请交易所的API，用户的资金全部在交易所，并不需要存入执行体，并且API只要不开放提现的权限，执行体是无法对用户的资金进行操作的

## 量化交易执行体支持哪些交易所？
第一期将支持欧易，第二期将支持币安，目前第一期程序正在内测中，内测结束将提供下载开放

## 量化交易云的收益如何？
量化交易追求的不是利益最大化，而是风险最小化，实现稳定收益才是量化交易最终目标，量化交易云端通过海量数据进行分析，只有经过运算得到的结果准确率达到一定高度的时候才会进行建模，执行体是依据云端模型进行交易的，所以你会发现目前每天完成的交易并不多，因为云端服务器还在不断的进行机器学习，随着学习的时间越长，通过学习所建模型就会越多，模型越多，交易就会越频繁，在保证准确性的前提下增加数量才能使收益持续稳定。
