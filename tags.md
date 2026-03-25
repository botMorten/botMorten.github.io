---
layout: page
title: Topics
permalink: /tags/
---

{% assign sorted_categories = site.categories | sort %}

{% if sorted_categories.size > 0 %}
  {% for category in sorted_categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>({{ post.date | date: "%Y-%m-%d" }})</small>
    </li>
    {% endfor %}
  </ul>
  {% endfor %}
{% else %}
  <p>No topics yet. The bot is probably busy fixing template UX somewhere.</p>
{% endif %}
