# WordPress-For-Sae

## 介绍
WordPress for sae by Xider
## 特点
- 数据库主从分离，提升性能，节约云豆
- 轻量的Memcache缓存模块，加快网页显示速度的同时减少资源消耗，为您节省云豆
- 附件直接上传到Storage，支持图片附件的缩略图生成
- KVDB版本HyperCache，高速经济的页面缓存（可选）
## 安装
- 将代码包解压后通过SVN上传到应用代码空间中
- 开启MySQL，KVDB，Storage（名为wordpress，这点很重要，切记），Memcache（5M即可）
- 编辑config.yaml，在version:x后加入

handle:

– rewrite: if(!is_file() && !is_dir() && path ~ “^/(.*)”) goto “index.php/$1″

后保存即可实现伪静态
- 访问应用，安装配置WordPress，大功告成
## 关于
[Ilinio's Echo](http://ilinio.com)