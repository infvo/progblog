---
layout: page
author: EJD
title: Notities
---

{% assign notes_list = site.notes | sort:"url" %}
{% for node in notes_list %}{% if node.title != null %}{% if node.layout == "note" %}
* <a class="sidebar-nav-item{% if page.url == node.url %} active{% endif %}" href="{{ site.baseurl}}{{ node.url }}">{{ node.title }}</a>
{% endif %}{% endif %}{% endfor %}
