# 钢材重量计算器支持站

静态站点，用于 App Store 隐私政策和技术支持页。不要把 iOS 源码放到这个站点仓库。

## 本地预览

```bash
python3 -m http.server 8000 --directory release/support-site
```

打开：

- http://127.0.0.1:8000/
- http://127.0.0.1:8000/privacy/
- http://127.0.0.1:8000/support/

## 发布

1. 用已登录的 GitHub 账号新建**公开**仓库 `steel-weight-support`。
2. 只上传本目录内容，不要上传 App 工程。
3. GitHub Pages 选择默认分支根目录。
4. 自定义域名为 `app.maomaoxingqiu.xin`（已有 `CNAME`）。
5. 在阿里云 DNS 仅增加：

```text
Type: CNAME
Host: app
Value: <github-user>.github.io
```

不要改根域名 `@` 记录，也不要改现有北京服务器。

6. 在 GitHub Pages 启用 HTTPS，再验证：

- https://app.maomaoxingqiu.xin/privacy/
- https://app.maomaoxingqiu.xin/support/

公开联系邮箱确认后，把邮箱补进 `privacy/index.html` 和 `support/index.html`。
