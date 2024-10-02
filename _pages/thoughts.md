---
layout: archive  # 这是指定布局文件，通常是 default 或 archive，控制页面的整体外观和结构。
title: "Thoughts"  # 这是页面的标题，会显示在页面的顶部和浏览器标签中。
permalink: /Thoughts/  # 这是页面的 URL 路径，访问这个页面时的网址会是 http://your-site/Thoughts/
---


<ul>
  {% for post in site.posts %}
    <li style="list-style-type: none; margin-bottom: 40px; display: flex; align-items: center;">  <!-- align-items: center 保证图片和文字垂直居中对齐 -->

      <!-- 左侧图片部分，设定固定大小 -->
      <div style="flex-shrink: 0;">
        <img src="{{ post.image }}" alt="{{ post.title }}" style="width: 200px; height: 150px; object-fit: cover; margin-right: 20px;">  <!-- 固定图片宽度为200px，高度150px，object-fit: cover 保证图片按比例裁剪 -->
      </div>

      <!-- 右侧文字内容部分，确保与图片居中对齐 -->
      <div style="display: flex; flex-direction: column; justify-content: center; max-width: 600px;"> <!-- max-width 限制文字区域的宽度，使其不占据太多空间 -->
        <h2>{{ post.title }}</h2>  <!-- 文章标题，不跳转 -->
        <p>
          {{ post.excerpt }} <!-- 简介 -->
          <a href="{{ post.external_url }}" target="_blank" rel="noopener noreferrer" style="margin-left: 10px;">Read more</a>  <!-- "Read more" 链接放在简介之后，保持在同一行，margin-left 添加间距 -->
        </p>
      </div>

    </li>
  {% endfor %}
</ul>
