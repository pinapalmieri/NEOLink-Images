---
title: Summary
layout: default
---

# 📄 Summary of All Pages

<ul>
  {% assign pages = site.pages
      | where_exp: "p", "p.url != '/404.html'"
      | where_exp: "p", "p.url != '/index.html'"
      | sort: "url" %}

  {% for p in pages %}
    <li>
      <a p.url | relative_url }}{{ p.title | default: p.url }}</a>
    </li>
  {% endfor %}
</ul>
