# 个人作品集网站

康宁的个人作品集（静态站点），由 Netlify 从本仓库自动部署。

## 目录结构

```
index.html          入口页
assets/             打包后的 JS / CSS（文件名带 hash）
images/             项目配图
favicon.svg         站点图标
icons.svg           图标雪碧图
netlify.toml        Netlify 配置（publish = "."）
```

## 部署

- 发布目录：仓库根目录（`netlify.toml` 里 `publish = "."`）
- 无构建命令，纯静态文件
- 推送到 `main` 分支后 Netlify 自动重新部署

## 如何更新网站

1. 拿到新的部署包（含 `index.html` / `assets/` / `images/`）
2. 清空本仓库里的 `index.html`、`assets/`、`images/`、`favicon.svg`、`icons.svg`（保留 `.git` 和 `netlify.toml`）
3. 把新部署包内的文件复制到仓库根目录
4. 提交并推送：

```bash
git add -A
git commit -m "更新网站内容"
git push origin main
```

5. 等 Netlify 自动部署完成，刷新线上地址即可
