---
layout: default
title: Tag
permalink: /tag/
---
<!-- ref.
* https://github.com/codinfox/codinfox-lanyon/blob/dev/blog/tags.html
* http://stackoverflow.com/a/18221512
-->
{% assign sorted_tags = site.tags | sort %}
<div class="list-of-tag">
    {% for tag in sorted_tags %}
    <h3 href="#{{ tag[0] }}">{{ tag[0] }}</h3>
    <ul>
        {% for post in tag[1] %}
        <li>
            <a class="post-link" href="{{ site.baseurl }}{{ post.url }}">
            {{ post.title }}
            </a>
            <span class="post-meta">({{ post.date | date: "%Y-%m-%d" }})</span>
        </li>
        {% endfor %}
    </ul>
    {% endfor %}
</div>
