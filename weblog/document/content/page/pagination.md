---
title: Pagination
---

Just add the following to your layout files:

```html
{% for article in articles %}
<div class="article">
    <div><a href="{{article.url}}">{{article.title}}</a></div>
    <div>{{article.content}}</div>
    <div>{% if article.date %}{{article.date | date('Y-m-d H:i')}}{% endif %}</div>
</div>
{% endfor %}

<div class="pagination">
  {% if paginator.previous_page %}
    <span class="newer"><a href="{{paginator.previous_url}}" class="previous">Newer Posts</a></span>
  {% endif %}
  {% if paginator.next_page %}
    <span class="older"><a href="{{paginator.next_url}}" class="next">Older Posts</a></span>
  {% endif %}
</div>
```

And you are done.