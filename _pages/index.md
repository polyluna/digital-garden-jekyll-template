---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

I'm Luna. You may also know me as _polyluna_, currently an avid zk learner.
Previously I worked in management consulting and UX/UI design. 

<strong>Writing</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    {% if note.title != "xxx" %}
      <li>
        {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
