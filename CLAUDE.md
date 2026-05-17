# Image Hosting Repo

图床仓库，存储 Litura 网站和 Nonconsensus 博客的所有图片，通过 jsDelivr CDN 提供访问。

## 目录结构

```
.
├── litura/
│   ├── blog/        # Litura 博客图片
│   └── fish-test/   # fish-test 功能头像图（PNG，16种组合）
└── nonconsensus/    # Nonconsensus 个人博客图片
```

## CDN 链接格式

```
https://cdn.jsdelivr.net/gh/weilaidewakaka/litura-image@main/<路径>
```

示例：
- `litura/blog/fishing-app-guide-cover.jpg` → Litura 博客封面
- `nonconsensus/2026-03-06-203017-5dd716fd.jpg` → Nonconsensus 文章图片

## 关联项目

- **Litura-web** (`~/project/Litura-web`) — 引用 `litura/` 下的图片
- **Nonconsensus Blog** (`~/project/nonconsensus-blog`) — 引用 `nonconsensus/` 下的图片

## 上传新图片

直接将图片放入对应目录，commit 并 push 到 main 即可。命名规范：
- Litura 博客：语义化名称，如 `fishing-app-guide-cover.jpg`
- Nonconsensus：带时间戳，如 `2026-03-06-203017-5dd716fd.jpg`

## 注意

- 移动或重命名图片后，必须同步更新 Litura-web 和 nonconsensus-blog 中的 CDN 引用
- fish-test 图片由代码动态拼接路径（`fish-test/{code}.png`），不要改文件名
