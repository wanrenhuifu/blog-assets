# blog-assets

[wanrenhuifu.github.io](https://wanrenhuifu.github.io) 的图片资源仓库。

正文配图等静态资源放在这里、通过 CDN 引用，而不是塞进博客仓库 ——
文章图片往往几 MB，放进源码仓库会让 clone 变慢、也把内容与代码混在一起。

## 引用方式

```
https://cdn.jsdelivr.net/gh/wanrenhuifu/blog-assets@<ref>/<path>
```

`<ref>` 用标签或提交哈希（如 `@v1`、`@a1b2c3d`），不要用 `main` ——
jsDelivr 对 `main` 有缓存，换图后要等缓存过期；钉住版本还能保证旧文章不会因为
新图覆盖旧文件而变样。

## 目录

```
images/     # 文章配图，按用途命名
friends/    # 友链头像，文件名 = 对方的 GitHub 用户名（小写）
```

## 关于版本标签

新增图片就加一个新标签（`v1`、`v2`…），引用钉在你引入它的那一版。
旧引用不必跟着改 —— 文件是只增不改的，旧标签永远指向当时那份内容，
也就不会因为后来覆盖同名文件而让旧文章变样。
