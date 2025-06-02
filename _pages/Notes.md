---
layout: archive
title: "Notes"
permalink: /Notes/
author_profile: true
---

{% include base_path %}




## 111

{% assign paths = "nameofthemd.md" | split: "," %}

{% for post in site.Notes reversed %}
  {% for path in paths %}
    {% if post.path contains path %}
      {% include archive-single.html %}
      {% break %}
    {% endif %}
  {% endfor %}
{% endfor %}
