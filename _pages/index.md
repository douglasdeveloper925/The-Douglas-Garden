---
layout: page
title: Home
id: home
permalink: /
---

<div id="hero" style="background-image: url('{{ '/assets/images/welcome.svg' | relative_url }}'); background-size: cover; background-position: center right; min-height:80vh; display:flex; align-items:center; padding: 4rem 1rem; border-radius: 8px; margin-bottom: 1.5rem;">
  <div style="max-width: 64rem; margin: 0 auto; background: rgba(15,23,42,0.12); padding: 2.5rem; border-radius: 8px; backdrop-filter: blur(3px);">
    <h1 style="margin:0; line-height:1.05;">Wayne Douglas: notes and inner dialogue.</h1>
    <p style="margin:0.75rem 0 0; color:#0f172a;">Let me divert your attention to <strong>[[Getting Started]]</strong> to begin exploring.</p>
  </div>
</div>

This online dialogue is a place where I can write freely and organize my notes on [Personal Development] and Transformation. See also my personal website  [my personal website here](https://challengeyourself.tech).

There is also information and resources about various other topics such as [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).

<strong>Recent Notes in no particular order</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
