---
layout: page
title: 点滴
---


{% for category in site.categories %}
{% if category.first == 'life'%}
<h2>{{ category | first }}</h2>
<ul class="arc-list">
    {% for post in category.last %}
        <li>{{ post.date | date:"%d/%m/%Y"}}<a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
{% endif%}
{% endfor %}