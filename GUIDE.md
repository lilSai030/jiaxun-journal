# Editing your Jiaxun Journal site (中文指南)

## 你平时只需要做的事

打开 https://app.pagescms.org/ ，用 GitHub 登录，选中你的网站仓库。

- **Homepage text**：修改首页介绍、About、Contact。
- **Projects and research**：增加 / 修改研究与社区项目。
- **Writing and games**：增加 / 修改小说、散文、游戏作品。

点击 New 创建条目，填写 Title、Date、Category、Summary，在大文本框中编辑正文。确保 **Publish on site** 打开，保存。保存会在 GitHub 创建一次提交。GitHub Pages 完成自动构建后，网站内容更新。

## 一次性的发布配置

1. 注册或登录 GitHub：https://github.com/ 。
2. 创建一个 **Public** repository，例如 `jiaxun-journal`。免费账户使用 GitHub Pages 发布时，公开仓库最简单。**注意：公开仓库中的文件和 Markdown 正文也会公开，不要上传任何隐私、采访原始数据、未获许可截图或未准备发布的完整手稿**。
3. 上传本压缩包解压后的**所有文件和文件夹**，包括隐藏文件 `.pages.yml`。不要只上传 ZIP。
4. 仓库 → Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save。GitHub Pages 会根据 `_config.yml` 和集合内容构建网站。
5. 打开 https://app.pagescms.org/ → GitHub 登录 → 安装/授权 Pages CMS GitHub App，仅给这个仓库权限 → 选择仓库。它会读取 `.pages.yml` 并显示内容编辑器。
6. 网站地址通常为 `https://你的GitHub用户名.github.io/jiaxun-journal/`，具体地址以 GitHub Settings → Pages 显示的地址为准。

## 关于本地预览

本项目采用 Jekyll 模板：**直接双击 index.html 不会完整渲染动态作品卡片**，因为这些内容要由 GitHub Pages 编译。请以上线后的 GitHub Pages 地址为准。若要本地完整预览，需要安装 Ruby/Jekyll（零代码使用者不必安装）。

## 重要提示

- 首页原有的大量固定项目文案仍在 `index.html` 内，CMS 目前管理首页关键介绍字段和新的 Archive 内容条目；如果以后想让所有段落都能点开编辑，还需要进一步拆分。
- 新建作品页面地址会自动生成，并在 Archive 中出现。
- 不要在 GitHub CMS 中发布私人原稿和第三方个人资料；即使将 Published 设为 false，内容仍存在于公开仓库中。不要用公开仓库储存私密草稿。
- 如果更改仓库名称或使用自定义域名，可能需要调整 `_config.yml` 的 `baseurl` / `url`。当前 `_config.yml` 已配置 `baseurl: /jiaxun-journal`，因此请将仓库命名为 `jiaxun-journal`。如果你换了仓库名称，请同步修改这个 baseurl。
