---
layout: post
permalink: /tags
title: Tags
description: Articles listed by tags.
author: ""
---

{% for tag in site.tags %}
  <h3 id="{{tag[0]}}">{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li>{{ post.date }} <a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}