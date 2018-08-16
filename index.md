---
layout: index
title: "Dilanka's Blog"
subtitle: by Dilanka
---

Here's a collection of random scribbles written by Dilanka. Feel free to browse around.


{% capture numposts %}{{ site.posts | size }}{% endcapture %}
{% if numposts != '0' %}
## Blog posts by year

{% for post in site.posts %}{% assign currentyear = post.date | date: "%Y" %}{% if currentyear != prevyear %}
### {{ currentyear }}
{% assign prevyear = currentyear %}{% endif %} - [{{ post.title }}]({{ site.baseurl }}{{ post.url }}) - {{ post.date | date: '%B %-d' }}
{% endfor %}
{% endif %}


