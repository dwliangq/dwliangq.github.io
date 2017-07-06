## 选择哪种缓存方案

在优化系统时，我们一般会考虑到缓存的使用。而现有的缓存方案不外乎就是本地缓存、远程缓存，至于选择哪一种缓存作为方案，标准答案就是看情况。这个就比较尴尬了，这种答案最不利于团队成员的开发。大家都看情况，肯定是各种情况。

### 双双对比

# 本地缓存
本地缓存我以前用到的有两种：
## 1 集合存储
这种方案最为简单，使用spring自提供的任务提供周期性数据同步刷新，存放的数据放在离你最近的地方
## 2 Ehcache
作为成熟的缓存框架，Ehcache无疑还是最轻量级的。整包大小几百K，无需服务器，无需单独部署。一键引用，再加个xml配置文件就解决了。而且与Spring结合良好的注解方式不用我们再去重新去拦截。支持FIFO、LUR、LFU等缓存过期策略，支持Listener的方式进行缓存刷新，支持最大空闲时间、最大失效时间设置。一个Ehcache可以配置多个缓存方案用于不用的服务，只需要一行配置就搞定。缓存存放策略也由你决定，恶汉式？懒汉式？都可以。

# 远程缓存
## Redis
这里只介绍Redis，大家肯定也想到memcache。至于这两者选择哪个？这个就不多做解释了，网上很多对比文章。
Redis无疑是非常强大的，各家公司都在使用Redis作为分布式缓存解决方案。一般公司都有自己专门的Reids集群，这对开发人员来说就比较简单了，调用下API就可以了。



```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/dwliangq/dwliangq.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
