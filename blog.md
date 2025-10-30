---
layout: page
title: Beiträge
permalink: /blog/
---

# Aktuelles & Beiträge

Hier findest du alle bisherigen CityWalks, News und Updates von **Dorfplatz TV**.

{% for post in site.posts %}
<div style="border:1px solid #eee; border-radius:8px; padding:1rem; margin-bottom:1.5rem; max-width:860px; margin-left:auto; margin-right:auto;">
  <h3 style="margin-top:0;">
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </h3>
  {% if post.subtitle %}
    <p><em>{{ post.subtitle }}</em></p>
  {% endif %}
  <small>{{ post.date | date: "%-d.%m.%Y" }}{% if post.tags %} • {{ post.tags | join: ", " }}{% endif %}</small>

  {% if post.thumbnail-img %}
    <div style="text-align:center; margin:1rem 0;">
      <img src="{{ post.thumbnail-img }}" alt="{{ post.title }}" style="max-width:100%; border-radius:4px;">
    </div>
  {% endif %}

  <p>{{ post.excerpt | strip_html | truncate: 260 }}</p>
  <a class="btn btn-primary" href="{{ post.url | relative_url }}">Weiterlesen</a>
</div>
{% endfor %}
