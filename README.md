# TypeBeat — 在线歌词打字对战（纯前端 Demo）

这是一个**无需后端**的静态网页，支持：
- 公共领域示例文本（Amazing Grace、Sonnet 18 等）
- 粘贴你**有权使用**的英文歌词/文本
- WPM、准确率、进度与 30/60/120 秒计时模式
- 大小写/标点/空白规范化开关

> 版权提示：请勿内置完整的受版权保护歌词；如要练习，可粘贴到页面中使用。

## 一键上线（任选其一）

### 方案 A：GitHub Pages（纯静态免费）
1. 新建仓库，例如 `typebeat-demo`，把本目录的文件上传。
2. 进入仓库 Settings → Pages，选择 `main` 分支的根目录 `/root`，保存。
3. 几十秒后会生成一个公开网址，分享给同学即可“联网使用”。

### 方案 B：Netlify（拖拽上传）
1. 访问 Netlify，登录后点「Add new site」→「Deploy manually」。
2. 将本目录**打包成 zip** 拖进去即可，生成一个公开链接。

### 方案 C：Vercel（零配置）
1. 新建项目，Import 你的 GitHub 仓库。
2. Framework 选择「Other」，Build & Output 留空，Output 目录为根目录。
3. 部署完成即可获得一个公开域名。

## 自行接入歌词 API（可选进阶）
当前版本不包含联网取词。要实现「按歌名搜索并拉取歌词」：
- 建议在你自己的后端里对接合法歌词数据源（带鉴权与缓存），
- 前端用 `fetch('/api/lyrics?q=xxx')` 获取 `{title, artist, text}` 再 `loadText()`，
- 注意版权与使用条款，避免直接在前端调用第三方受限接口。

## 本地预览
直接双击 `index.html` 即可在浏览器打开。