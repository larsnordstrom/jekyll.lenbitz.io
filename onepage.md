---
layout: onepage
# title: OnePage layout
permalink: /onepage/
---

  <ul class="post-list">
	{% assign sorted-posts = site.posts | where: "categories","fpv" %}
    {% for post in site.posts limit: 3 %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>