---
layout: page
---
{% include JB/setup %}

<div class="row-fluid">
  <div class="span9">
    {% for post in site.posts %}
      <div class="well">
        <p><h2><a href="{{ post.url }}">{{ post.title }}</a></h2></p>
        <p>{{ post.date | date_to_string }}</p>
        <p>{{ post.content | strip_html | truncatewords: 70 }}</p>
        <p><a href="{{ post.url }}">阅读全文 ...</a></p>
      </div>
    {% endfor %}
  </div>
  <div class="span3">
    <div id='tag_cloud'>
      {% for tag in site.tags %}
        <a href="#{{ tag[0] }}" title="{{ tag[0] }}" rel="{{ tag[1].size }}">{{ tag[0] }}</a>
      {% endfor %}
    </div>
  </div>
</div>

