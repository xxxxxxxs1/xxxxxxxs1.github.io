---
layout: page
title: 文章列表
permalink: /archives/
---

{% for post in site.posts %}

<div class="archive-item">

  <div class="archive-date">
    {{ post.date | date: "%Y-%m-%d" }}

    {% if post.categories %}
      · {{ post.categories }}
    {% endif %}
  </div>

  <h2>
    <a href="{{ post.url | relative_url }}">
      {{ post.title }}
    </a>
  </h2>

</div>

{% endfor %}
