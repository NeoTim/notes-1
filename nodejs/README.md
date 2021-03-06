# 基础知识
<!-- toc -->

## 升级 nodejs 和 npm
升级nodejs: [nvm](https://github.com/creationix/nvm)
```
nvm install <version>
nvm alias default <version>
```

## 版本号
```bash
*: 任意版本
1.1.0: 指定版本
~1.1.0: >=1.1.0 && < 1.2.0
^1.1.0: >=1.1.0 && < 2.0.0
```
其中 `~` 和 `^` 两个前缀让人比较迷惑，简单的来说：  
* `~` 前缀表示，安装大于指定的这个版本，并且匹配到 `x.y.z` 中 `z` 最新的版本。  
* `^` 前缀在 `^0.y.z` 时的表现和 `~0.y.z` 是一样的，然而 `^1.y.z` 的时候，就会 匹配到 `y` 和 `z` 都是最新的版本。  
* 特殊的是，当版本号为 `^0.0.z` 或者 `~0.0.z` 的时候，考虑到 `0.0.z` 是一个不稳定版本， 所以它们都相当于 `=0.0.z`。

## 修改全局路径
```
npm config set prefix "D:\nodejs\node_global"
```

## 修复npm安装时报VCBuild不存在的错误

```
npm install --global --production windows-build-tools
```