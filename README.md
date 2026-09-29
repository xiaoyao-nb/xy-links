# xy-links
这是一个毛玻璃效果，有后台的网站导航，瞎搞的
一个支持暗黑毛玻璃风格、多主题切换、SEO可控、外站安全跳转的个人导航站点。
演示站:https://xy-links.nbnb.mom/
发行页:https://xy.nki.pw/index.php/archives/18/

## 📁 项目结构

```
 xy-links/
├── index.php              # 前端首页（导航展示）
├── robots.txt             # 搜索引擎爬虫规则
├── sitemap.xml            # 站点地图
├── README.md              # 本文件
│
├── config/
│   └── database.php  # 数据库配置示例
│
├── includes/
│   └── functions.php      # 通用函数库
│
├── admin/                 # 后台管理
│   ├── index.php          # 后台入口
│   ├── login.php          # 登录页
│   ├── ajax.php           # AJAX接口
│   └── pages/            # 后台各页面
│       ├── dashboard.php  # 仪表盘
│       ├── links.php      # 导航管理
│       ├── seo.php        # SEO设置
│       ├── themes.php     # 主题管理
│       ├── settings.php   # 站点设置
│       └── password.php   # 修改密码
│
└── sql/
    └── init.sql           # 数据库初始化SQL
```

## 🛠️ 部署步骤

### 1. 环境要求
- PHP 7.4+
- MySQL 5.7+ / MariaDB 10.2+
- Apache / Nginx

### 2. 导入数据库
```bash
mysql -u root -p < sql/init.sql
```

### 3. 配置数据库连接

# 编辑 database.php，填入你的数据库信息


### 4. 修改站点配置
编辑 `config/database.php`：
```php
define('SITE_URL', 'https://你的域名.com');  // 改为你的域名
```

### 5. 设置权限
```bash
chmod 755 -R nav-site/
chmod 666 nav-site/sitemap.xml
```

### 6. 访问
- 前台：`https://你的域名.com/`
- 后台：`https://你的域名.com/admin/`
- 默认账号：`admin` / `admin123`（**请务必修改**）

## ✨ 功能特性

### 前端
- 🎨 6款内置主题（暗黑毛玻璃/星空紫/极光绿/日落橙/科技蓝/粉樱）
- ✨ 毛玻璃 + 背景粒子动画
- 🔍 实时搜索过滤
- 📂 分类标签切换
- 🛡️ 外站跳转安全确认弹窗
- 📱 响应式设计，移动端适配

### 后端
- 🔐 登录鉴权（密码bcrypt加密）
- 🔗 导航链接 CRUD（增删改查）
- 🎨 主题管理（切换/自定义/删除）
- 🔍 SEO完整控制（Title/Description/Keywords/Robots/Sitemap）
- ⚙️ 站点设置（备案号/版权/底部信息）
- 🔑 修改密码

## 🔍 SEO优化说明

1. **默认允许爬虫** - robots.txt 设为 `Allow: /`
2. **自动生成Sitemap** - 后台可一键重新生成
3. **完整Meta标签** - title/description/keywords/OG/Twitter Card
4. **提交搜索引擎**：
   - 百度站长平台：https://ziyuan.baidu.com
   - Google Search Console：https://search.google.com/search-console
   - Bing Webmaster：https://www.bing.com/webmasters

## 🎨 自定义主题

在后台「主题管理」→「自定义主题」中，可以调整：
- 主背景色 / 毛玻璃背景 / 悬停背景
- 主文字色 / 次文字色
- 强调色（主色调）/ 发光色
- 边框颜色 / 卡片阴影
- 模糊度 / 渐变背景 / 圆角

所有修改实时预览，保存后即可在前台使用。

## 🛡️ 安全建议

1. 修改默认管理员密码
2. 修改后台路径（重命名 `admin` 文件夹 + 同步修改 `index.php` 中的链接）
3. 配置 HTTPS
4. 定期备份数据库
5. 可在 `.htaccess` 中增加额外IP限制

## 📝 License

MIT License - 自由使用、修改、分发

## 版权©️声明
小尧制作
