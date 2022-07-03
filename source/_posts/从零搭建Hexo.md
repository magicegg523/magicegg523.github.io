---
title: 从零搭建Hexo
date: 2022-07-02 22:11:51
tags:

---

- 官网地址：

  [Hexo](https://hexo.io/zh-cn/)

- 安装：

  npm install hexo-cli -g

- 生成Blog：

  hexo init

- 启动Blog：

  hexo s

- 创建文章：

  hexo n "title"

- 生成文件：

  hexo g



接下来，在github上新建一个仓库，注意仓库名必须为用户名.github.io

回到本地blog目录下，在命令行工具中输入npm install hexo-deployer-git

修改目录下的_config.yml文件，将最后几行修改为：

```yaml
deploy:
  type: 'git'
  repo: 'https://github.com/magicegg523/magicegg523.github.io.git'
  branch: 'main'
```



- 发布文章：

  hexo d

  

如果遇到无法验证的情况，可以将配置文件修改为ssh的连接方式：

```yaml
deploy:
  type: 'git'
  repo: 'git@github.com:magicegg523/magicegg523.github.io.git'
  branch: 'main'
```



如果看到如下提示说明推送成功：

INFO  Deploy done: git



这时可以通过域名访问blog:

[Hexo (magicegg523.github.io)](https://magicegg523.github.io/)





安装主题：

git clone https://github.com/litten/hexo-theme-yilia.git themes.yilia

hexo clean

hexo g



