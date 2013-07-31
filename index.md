---
layout: default
---
 
{% assign page = site.posts.first %}
{% assign content = page.content %}
{% include JB/setup %}

<article class="unit-article layout-post">
  <div class="unit-inner unit-article-inner">
    <div class="content">
      <header>
        <div class="unit-head">
          <div class="unit-inner unit-head-inner">
            <a href="{{ page.url }}"><h1 class="h2 entry-title">{{ page.title }}</h1></a>
          </div><!-- unit-inner -->
        </div><!-- unit-head -->
      </header>

      <div class="bd">
        <div class="entry-content">
          {{ content }}
        </div><!-- entry-content -->
      </div><!-- bd -->
      <footer class="unit-foot">
        <div class="unit-inner unit-foot-inner">
          <nav class="pagination">
            <ul>
              {% if page.previous %}
              <li class="prev"><a class="internal" rel="prev"  href="{{ page.previous.url }}" title="View {{ page.previous.title }}">&laquo; {{ page.previous.title }}</a></li>
              {% endif %}
              {% if page.previous and page.next %}
              <li class="pipe"> | </li>
              {% endif %}
              {% if page.next %}
              <li class="next"><a class="internal" rel="next"  href="{{ page.next.url }}" title="View {{ page.next.title }}">{{ page.next.title }} &raquo;</a></li>
              {% endif %}
            </ul>
          </nav>
          <p class="gotop">
            <a href="#page">Back to Top</a>
          </p>
        </div>
      </footer>

    </div><!-- content -->
  </div><!-- unit-inner -->
</article>
