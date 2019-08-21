# YoudaoKadaBlog
## 1. 有道卡搭早读博客
不定期更新推荐阅读文章，详情见<https://github.com/youdaokada/YoudaoKada.github.io>

## 2. 工程初始化
早读系统由hexo驱动，采用pure主题，并将 `theme/pure` 作为项目的子模块（git submodule）。拉取时使用 `git clone --recursive` 命令, git 就会自动初始化并更新仓库中的每一个子模块。

```
git clone --recursive https://github.com/youdaokada/YoudaoKadaBlog.git
```
若未添加 `--recursive` 参数，在 clone 后的项目中可以通过运行两个命令:

1. `git submodule init` 初始化本地配置文件
2. `git submodule update` 从该项目中抓取所有数据并检出父项目中列出的合适的提交。

## 3. 开始写早读
### 3.1 创建文章
> 文章按季度进行归档，使用 `hexo new` 的方式来创建文章，完整的命令如下。
>
> 运行结束之后，会在2018Q4目录下生成 `前端早读-20181019.md` 文件；或者直接复制之前的文章做修改，然后下一步就可以使用markdown语法开始编辑了。

```
hexo new post -p /2019Q3/前端早读-20190821
```

#### 早读样例
参考样例，完成 标题、日期、目录、作者、链接及推荐语。
![参考样例](https://s2.ax1x.com/2019/08/21/mNaIMD.jpg)


### 3.2 部署
> 将早读文章推送到博客仓库
```
hexo generate
hexo deploy
```

### 3.3 代码推送
> 不要忘记将文件推送到远端
```
git push --recurse-submodules=check
```

## 4. 注意事项
1.注意格式：文章链接与推荐语之间使用一个换行符隔开；不同的文章之间再隔一行。

2.注意日期：举个例子，如果轮到我周一发早读，无论是哪天完成，日期都要写成周一的日期。

3.注意不要忘记推送至远端仓库。
