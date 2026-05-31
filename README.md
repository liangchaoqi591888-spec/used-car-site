# 驰选二手车网站上线和车源上传

这是一个纯静态二手车展示网站，可以免费部署到 GitHub Pages。

## 文件说明

- `index.html`：对外访问的网站首页。
- `admin.html`：车源管理页，用来新增、编辑、删除车源。
- `data/cars.js`：网站读取的车源数据。
- `.nojekyll`：让 GitHub Pages 按普通静态文件发布。

## 免费上线方式：GitHub Pages

1. 新建一个 GitHub 仓库，例如 `used-car-site`。
2. 把本文件夹里的所有文件上传到仓库根目录。
3. 在仓库页面进入 `Settings` → `Pages`。
4. `Build and deployment` 选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/root`，保存。
6. 等待 GitHub Pages 部署完成后，会得到一个类似 `https://你的用户名.github.io/used-car-site/` 的网址。

## 上传和更新车源

1. 打开 `admin.html`。
2. 填写车辆信息，可以使用图片 URL，也可以选择本地图片。
3. 点击“保存车源”。
4. 点击“导出 cars.js”。
5. 用导出的 `cars.js` 替换仓库里的 `data/cars.js`。
6. 提交到 GitHub 后，GitHub Pages 会自动更新网站。

## 图片建议

- 少量车源：可以直接在 `admin.html` 上传本地图片，导出的 `cars.js` 会包含图片数据。
- 车源很多或图片很大：建议把图片上传到图床、GitHub 仓库或对象存储，然后在管理页填写图片 URL。

## 注意

这个版本没有后端数据库，适合免费、轻量、容易维护的展示网站。如果以后要做真正的在线后台登录、多人协作上传、客户线索保存，可以再升级到 Supabase、Firebase 或 Netlify CMS 等方案。
