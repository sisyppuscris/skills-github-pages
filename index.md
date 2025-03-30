---
# 头部配置（必须）
layout: home         # 使用主题的首页布局（网页5、网页7）
title: "我的博客"    # 页面标题（网页3、网页6）
permalink: /         # 页面访问路径（网页5）
author_profile: true # 是否显示作者信息栏（网页7）
header:
  image: /assets/images/header.jpg  # 头图路径（需自行创建/assets/images/文件夹）
---

<!-- 欢迎模块 -->
# 👋 欢迎来到我的博客！ {#welcome}
这里将记录我的技术思考与生活感悟，可通过下方导航栏快速定位内容。  
（提示：在此处添加简介，参考网页5的导航栏配置）

---

<!-- 最新文章列表 -->
## 📝 最新文章
{% raw %}{% for post in site.posts limit:5 %}{% endraw %}
<div class="post-item">
  <h3>
    <a href="{% raw %}{{ post.url | relative_url }}{% endraw %}">
      {% raw %}{{ post.title }}{% endraw %}
    </a>
  </h3>
  <small>{% raw %}{{ post.date | date: "%Y年%m月%d日" }}{% endraw %}</small>
  <p>{% raw %}{{ post.excerpt | strip_html | truncate: 100 }}{% endraw %}</p>
</div>
{% raw %}{% endfor %}{% endraw %}

> 提示：文章需按 `YYYY-MM-DD-title.md` 格式存储在 `_posts` 文件夹（网页2）

---

<!-- 分类导航 -->
## 🔍 内容分类
| [技术笔记](/categories/tech) | [生活随笔](/categories/life) | [项目实践](/categories/projects) |
|-----------------------------|------------------------------|----------------------------------|

> 提示：分类页需在 `_pages` 文件夹创建对应 Markdown 文件（网页5）

---

<!-- 页脚信息 -->
{% include footer.html %}  <!-- 引用主题的页脚组件（网页7） ```
