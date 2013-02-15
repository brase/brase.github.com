---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}

<ul class="posts">
{% for post in site.posts limit: 5 %}
  <div class="post_info">
    <li>
            <h2><a href="{{ post.url }}">{{ post.title }}</a>
            <span>({{ post.date | date:"%Y-%m-%d" }})</span></h2>
    </li>
    <br /> <span>{{ post.content | strip_html | truncatewords:75}} </span>
    
    <a href="{{ post.url }}">Read more</a>
    </div>
  {% endfor %}
</ul>