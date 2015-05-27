---
layout: default
title: Home
---

<div class="blog">

  <ul class="post-list">

    {% for post in site.posts %}
    
      <li class="post-item">

      	{% if post.image %}

		<figure>
			<img src="{{post.image}}" alt="{{post.title}}">
		</figure>
		      
    	{% endif %}

        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>

        <p>{{post.excerpt}}</p>

        <a href="{{site.url}}{{post.url}}">Read more</a>

      </li>

    {% endfor %}

  </ul>

</div>
