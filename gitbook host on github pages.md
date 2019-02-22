# gitbook host on github pages

[TOC]

Pages 是github类网站提供的免费的静态网页托管服务，既然GitBook能生成基于HTTML的静态电子书籍，那自然而然，我们就会有将GitBook静态页面发布到pages服务的需求。

除了能够将书籍发布到GitBook.com外，用户还可以将电子书发布到提供Pages服务的GitHub类站点上，如国内的oschina、coding.net等等。这样做有个好处，就是访问速度比gitbook.com快很多。

### 将书籍源码托管到git远端仓库

##### 将书籍编译成html文件

> gitbook build

##### 创建docs文件夹

> mv _book docs

GitHub pages托管服务只能展示html静态文件，gitbook项目中包含有原始的markdown文件以及编译之后的hmtl文件，编译生成的html文件默认保存在_book目录下，Github pages支持只展示docs目录中的文件，因此，将 _book重命名为docs，提交给github后可以直接展示。

##### 新建仓库

> git init

##### 添加文件

> git add .

##### 添加更新说明

> git commit -m 'commit something'

##### 推送到远端

> git push

### 自动化脚本

pushlish.sh

> gitbook build
> mv _book docs
> git add .
> git commit -m 'commit'  
> git push