# 超模公会网页发布说明

当前浏览器里的 `file:///C:/Users/.../index.html` 是本机文件地址，只有这台电脑能打开。想让公会其他人访问，需要把这个静态站发布到公网。

## 最省事方式

1. 使用项目根目录里的 `supermodel-guild-site.zip`。
2. 打开一个静态网站托管平台，例如 Netlify、Vercel、Cloudflare Pages 或 GitHub Pages。
3. 新建站点，把压缩包或解压后的整个文件夹上传。
4. 平台生成的 `https://...` 链接就是可以发给公会的访问地址。

## 文件说明

- `index.html`：网页内容
- `styles.css`：页面样式
- `script.js`：交互脚本
- `assets/supermodel-hero.png`：主视觉图片

## 临时局域网分享

如果只是在同一个 Wi-Fi 下给身边的人看，可以在这个目录运行：

```powershell
python -m http.server 8765 --bind 0.0.0.0
```

然后把本机局域网 IP 拼成：

```text
http://你的局域网IP:8765/
```

这个方式通常只适合同一网络内访问，不适合作为公会公网链接。
