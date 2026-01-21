---
layout: page
permalink: /publications/
title: Publications
description: Publications by categories in reversed chronological order.
nav: true
nav_order: 2
---

<div class="publications">

{% if site.data.publications %}
  <ul class="publications">
    {% for pub in site.data.publications %}
      {% if pub.selected %}
        <li>
          <!-- Authors -->
          <div class="pub-authors">{{ pub.author | raw }}</div>

          <!-- Paper title -->
          <div class="pub-title"><strong>{{ pub.title }}</strong></div>

          <!-- Venue / Journal -->
          {% if pub.journal %}
            <div class="pub-venue">{{ pub.journal | raw }}</div>
          {% endif %}

          <!-- Booktitle (normal, no bold) -->
          {% if pub.booktitle %}
            <div class="pub-venue">{{ pub.booktitle | raw }}</div>
          {% endif %}

          <!-- Note / acceptance rate -->
          {% if pub.note %}
            <div class="pub-note">{{ pub.note | raw }}</div>
          {% endif %}

          <!-- Links -->
          <div class="pub-links">
            {% if pub.url %}<a href="{{ pub.url }}" target="_blank">[link]</a>{% endif %}
            {% if pub.pdf %}<a href="{{ pub.pdf }}" target="_blank">[PDF]</a>{% endif %}
            {% if pub.slides %}<a href="{{ pub.slides }}" target="_blank">[Slides]</a>{% endif %}
          </div>
        </li>
      {% endif %}
    {% endfor %}
  </ul>
{% endif %}

</div>
