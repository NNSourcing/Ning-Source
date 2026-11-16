# 部署步骤（GitHub + Netlify + Decap CMS）

1. 在 GitHub 新建仓库，把本文件夹所有文件上传（根目录要有 index.html）。
2. 编辑 `admin/config.yml`：把 `repo:` 改成 `你的用户名/仓库名`。
3. Netlify → Add new site → Import from Git → 选该仓库。Build command 留空，Publish directory 填 `.`。
4. 让后台能登录：
   - GitHub → Settings → Developer settings → OAuth Apps → New，Homepage URL 填你的 Netlify 网址，Callback URL 填 `https://api.netlify.com/auth/done`，拿到 Client ID 和 Secret。
   - Netlify → Site configuration → Access & security → OAuth → Install provider → GitHub，填入 ID 和 Secret。
5. 打开 `你的网址/admin/` 用 GitHub 登录，即可修改页面内容，保存后自动发布。
6. 客户提交的表单在 Netlify → Forms 查看；Forms → Notifications 可设置邮件提醒。
7. 改邮箱、品牌名、价格都在后台完成；换域名在 Netlify → Domain management。
