### MkDocs 
MkDocs是一个快速、简单、华丽的静态网站生成器，适用于构建项目文档。文档源文件以Markdown编写，并使用一个YAML文件来进行配置。

> 为了手动安装MkDocs，你需要在系统上安装Python，以及Python包管理器pip。详情见 <https://hellowac.github.io/mkdocs-docs-zh/>
### 一、 运行

1. 下载依赖
```
pip install -r requirements.txt
```
2. 本地启动
```
mkdocs serve
```
3. 打包
```
mkdocs build
```
4. 部署到github pages
```
mkdocs gh-deploy
```
### 二、 配置

配置文件为 mkdocs.yml 各项配置见<https://squidfunk.github.io/mkdocs-material/setup/>

#### 新建页面
`docs/`目录作为页面的根路由，新建的目录和md文件作为子路由

例如：
```
docs/index.md       ---> http://127.0.0.1:8000/
docs/test1/index.md ---> http://127.0.0.1:8000/test1/
docs/test1/page1.md ---> http://127.0.0.1:8000/test1/page1/
```

#### 新建导航
新建页面之后，在 `mkdocs.yml` 中新建或修改`nav`配置,命名和层级如下：

```
nav:
  - 主页: index.md
  - 目录一:
    - 页面1: test1/page1.md
  - 目录二:
    - 页面2: test2/page2.md
```

