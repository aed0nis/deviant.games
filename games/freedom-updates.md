---
layout: page
title: "Freedom! – Updates & Handouts"
permalink: /games/freedom/updates/
game_id: freedom
---

{% assign game_updates = site.updates | where: "game_id", page.game_id | sort: "date" | reverse %}
<ul class="game-updates__list">
  {% for up in game_updates %}
    <li>
      <a href="{{ up.url | relative_url }}">{{ up.title }}</a>
      <span class="game-updates__date">{{ up.date | date: "%b %-d, %Y" }}</span>
      {% if up.kind %}
        <span class="game-updates__tag">{{ up.kind }}</span>
      {% endif %}
    </li>
  {% endfor %}
</ul>
