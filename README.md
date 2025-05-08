# community-announcements
# 小区公告数据仓库

这个仓库用于存储小区公告的JSON数据，通过GitHub Pages提供给小程序访问。

## 设置步骤

### 1. 创建GitHub仓库

1. 登录您的GitHub账号
2. 点击右上角的 "+" 按钮，选择 "New repository"
3. 仓库名称建议设为：`community-announcements`
4. 选择公开仓库（Public）
5. 勾选 "Initialize this repository with a README"
6. 点击 "Create repository"

### 2. 上传公告数据文件

1. 在仓库页面，点击 "Add file" > "Upload files"
2. 将 `announcements.json` 文件拖拽到上传区域
3. 在提交信息中填写 "添加公告数据文件"
4. 点击 "Commit changes"

### 3. 启用GitHub Pages

1. 在仓库页面，点击 "Settings"
2. 在左侧菜单中找到 "Pages"
3. 在 "Source" 部分，选择 "main" 分支
4. 点击 "Save"
5. 等待几分钟，GitHub Pages将被激活
6. 页面会显示您的GitHub Pages URL，格式为：`https://您的用户名.github.io/community-announcements/`

### 4. 更新小程序中的URL

1. 打开小程序项目中的 `pages/announcement/announcement.js` 文件
2. 找到 `announcementUrl` 变量
3. 将其值更新为您的GitHub Pages URL加上文件名：`https://您的用户名.github.io/community-announcements/announcements.json`

## 更新公告数据

当需要更新公告时，您可以：

1. 在GitHub仓库页面找到 `announcements.json` 文件
2. 点击文件名，然后点击编辑按钮（铅笔图标）
3. 按照现有格式添加新的公告项，确保每个公告都有唯一的ID
4. 在页面底部填写提交信息，如 "更新公告数据"
5. 点击 "Commit changes"

更新后，小程序将在下次刷新时自动获取最新的公告数据。

## 公告数据格式

```json
[
  {
    "id": "唯一ID",
    "title": "公告标题",
    "date": "发布日期（YYYY-MM-DD格式）",
    "summary": "公告摘要（简短描述）",
    "content": "公告完整内容（支持\n换行）"
  }
]
```

请确保JSON格式正确，否则可能导致小程序无法正确读取数据。
