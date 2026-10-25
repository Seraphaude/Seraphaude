---
layout: page
title: 索引
permalink: /tags/
---

{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
<h3>{{ tag[0] }}</h3>
<ul>
{% for post in tag[1] %}
<li>{{ post.date | date: site.minima.date_format }}　<a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}
