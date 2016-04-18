#RuffHelper
一个 Ruff 开发辅助工具，把常用的 rap 命令可视化操作。
使用 React + Electron 框架。
因为还没有做各种带选择的命令功能，目前只适合单人开发使用。

###原理
工作原理很简单，就是使用 node 子进程调用 rap 的命令,然后把返回的消息显示出来。
###问题
目前存在的问题主要是 rap 有一些带交互的命令不好处理。

大致分一下， rap 的命令主要有3种

1. 发出去不用管。类似 rap version \ rap deploy。只要把返回的消息打印出来就行了。
2. 需要输入内容。类似 rap init 中需要输入项目名称、版本号之类的。这种也比较好处理，因为要输入的 key 是固定的，分析字符串发现匹配的，把对应的 value 传进去就行了。
3. 需要选择的。比如很多时候有多个 wifi、开发板 之类的要选择。这种比较麻烦，因为返回的格式不是固定的，只能分析字符串，目前这种类型的还没做，以后有时间慢慢弄，或者看官方能不能支持一下，再加个-xxx 命令返回json之类的数据，然后弹出个面板让用户选择就方便了。

###调试开发流程
npm install 安装各种包,需要翻墙，可以使用 [cnpm](https://npm.taobao.org/)

1. npm run dev 启动 webpack，自动编译 react
2. npm run start 启动 electron
3. happy coding

###发布流程
见doc里面的文档

###完成的功能
1. ruff sdk 选择功能
2. ruff 项目管理功能

###todo list
1. 增加带选择功能的命令，比如 选择wifi输入密码
2. 固件升级功能
3. 制作安装包
4. 自动更新，不需要每次重新下载整个应用的包

###发布版本地址
[git最大附件25M，只能放百度网盘了](http://pan.baidu.com/s/1kVRI98b#path=%252Fruffhelper)








