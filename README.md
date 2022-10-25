# 旧版Hugo学术主题 | The old version of Hugo academic theme

Hexo+github.io是当前最广为人知的个人网站搭建方法，但Hexo的主题一般只适合于写博客，想构建个包含随笔，论文，代码，教程，博客等多重内容的个人网站并不很方便。我们经常可看到学术大牛们都会有个个人网站介绍自己的论文、团队、简历、博客等等的内容，比如 这个，实现这样的网站使用hexo上的各种主题配合插件自己折腾就稍显麻烦了，因此我们介绍Hugo+Academic主题+github.io构建复合型个人网站的方法。Hugo和Hexo很相似，都是静态网页生成器，Hugo基于go语言编写，速度飞快，配合异常好用的Academic主题，可方便的构建网站。
# 一、完成效果展示
![请添加图片描述](https://img-blog.csdnimg.cn/b83fbd82032345d9ab3c2673f1517c54.png)

[简陋版效果](https://Yiminghh.github.io)

[大佬效果1](https://shiruipan.github.io/)

[大佬效果2](https://linzhuyue.github.io/)

# 二、安装Hugo
参考 [Hugo中文文档](https://www.gohugo.org/)

注：有些设备安装完后需设置环境变量

# 三、生成模板网站
方法一：可以安装 [Hugo中文文档](https://www.gohugo.org/)中的的方法新建一个空的主页
方法二：我是直接fork [academic主题的模板](https://github.com/Yiminghh/hugo-academic-old-demo)（我这边用的是一个旧版的academic主题的[模板](https://github.com/Yiminghh/hugo-academic-old-demo)，基本就是把原主题的仓库退到了之前的版本，支持新版的Hugo extended，在“hugo extended v0.83.1”上实测可用。最新版的好像要用go语言，我运行时候总是出问题，而且我觉得旧版就挺好看的。）
- 注意仓库名称需要修改成 [github用户名].github.io
-  [github用户名].github.io 网址就能看到你的个人主页啦！！撒花！

后面就需要对模板内容进行修改了。

注：旧版和新版academic主题在feature上并没有很大差别（核心feature基本一致），[新版的文档](https://wowchemy.com/docs/)有很大的参考价值。


# 四、修改网站模板
我认为最快速的方法是直接阅读并修改exampleSite，里面提供的注释还算详细。




## 4.1 具体操作
1. 下载仓库到本地，然后在命令行中打开该文件夹，
2. 开启本地测试服务器
输入hugo server命令来启动测试服务器，@http://localhost:1313
hugo server会自动侦测源文件变动自动刷新页面，调试十分方便

![在这里插入图片描述](https://img-blog.csdnimg.cn/48299e1a027a46398fcada7f49b23eb5.png)
在浏览器中打开localhost:1313即可预览本地的运行效果。（可以实时显示修改情况）
把本地项目push到github就可以从 [github用户名].github.io 访问啦！

## 4.2 个性化配置
你需要修改全部文件都在博客根目录的以下文件夹中：

- config (很重要)
- content
- static

注释里都写明了文档链接，顺次捋一遍按自己需求修改即可。和hexo类似，Academic的内容由markdown文件表达，前面部分用 +++ 包起来的是用于指挥渲染的头信息，后面是正常的markdown内容。home文件夹下是首页各个组件的.md文件，我们可以调整各个组件.md文件中的active配置项来决定是否使用组件。

## 4.3 开启中英双语言
这边有一个 [博客](https://blog.csdn.net/leida_wt/article/details/104175919) 介绍开启中英双语言的方法，不过还没实践不知道是否可行，后面完成了再来更新。


# 五、其他
1. 发布文章如果有参数 draft ，记得将值设为 false，或者删除 draft，不然会被认定为草稿只能本地运行而不能运行到网站上。
2. 导航栏的图片修改在 ./themes/academic/assets/images/icon.png 路径下，找了半天终于找到了

目前还在瞎捣鼓阶段，把阶段性的搭建历程记录一下防止遗忘，也欢迎讨论交流。

