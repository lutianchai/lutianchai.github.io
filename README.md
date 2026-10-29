# 鹿添柴的个人主页

无需服务器或安装依赖的静态个人主页。

## 在线访问

https://lutianchai.github.io/

## 页面内容

- 个人介绍、B 站与 GitHub 入口。
- 星宇橙色、银色、深蓝色三种配色。
- 当前三个公开仓库的展示卡片：雨课堂刷课器、Android 模拟器工具箱和本主页。
- 三个预留作品位置。预留位置只是展示，不会跳转到空页面。
- 桌面三列、平板两列、手机单列，支持键盘导航与减少动态效果的系统偏好。

## 以后怎样添加项目

在 GitHub 打开 `index.html`，点击编辑，找到 `class="project-grid"`。

将任意一个 `class="project-card placeholder"` 的完整 `<li>…</li>` 替换成下面的项目卡片，填写自己的内容：

```html
<li class="project-card">
  <h3>项目名称</h3>
  <p class="project-description">用一两句话说明项目能做什么。</p>
  <a class="project-link"
     href="https://github.com/lutianchai/repository-name"
     aria-label="查看项目名称的 GitHub 仓库">
    查看项目 <span aria-hidden="true">↗</span>
  </a>
</li>
```

没有空位时，在 `project-grid` 的结束标签前继续添加卡片即可，页面会自动换行。项目使用静态卡片，不会自动同步 GitHub 仓库列表；发布新仓库后在这里补上一张即可。所有项目内容在关闭 JavaScript 时仍可访问。

## 修改其他内容

- 网页标题：`<title>`。
- 搜索简介：`meta name="description"`。
- 姓名：同步修改导航、`h1`（含 `aria-label`）、页脚和网页标题。
- 欢迎语：`class="hello"`。
- 项目区标题：`id="projects-title"`。
- B 站入口：搜索 `https://space.bilibili.com/487399025`。
- 配色与布局：在 `<style>` 中修改。

默认使用星宇橙色，每次重新打开恢复橙色。项目链接使用蓝色强调。

## 发布

修改并提交到 `main` 后，GitHub Pages 会自动更新。

首次配置：Settings → Pages → Deploy from a branch，选择 `main` 和 `/ (root)`。

设计参考 Apple 中国官网的简约排版、留白和蓝色链接，页面代码独立编写。
