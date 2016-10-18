---
layout: page
title: Categories
permalink: /categories/
---

{% for category in site.categories %}
### {{ category | first }}
<ol>
  {% for posts in category %}
    {% for post in posts %}
      {% if post.title %}
        <li><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
      {% endif %}
    {% endfor %}
  {% endfor %}
</ol>
{% endfor %}