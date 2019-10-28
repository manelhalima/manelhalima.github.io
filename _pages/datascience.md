---
layout:archive
permalink: /datascience/
title: "Datascience"
author_profile: true
header:
  image:"/images/logo2.png"
---
{% include base_path %}
{% include group-by-array collection=site.posts=group_items[forloop.index0] %}
{% for tag in group_names %}
  {%assign posts=group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}

