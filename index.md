---
layout: default
---
<p>オリジナル電子工作キットを製作・頒布しています。</p>
<h2>Works / 作品一覧</h2>
{% assign list = site.works | sort: "date" | reverse %}
{% for w in list %}
<div class="work">
  <a href="{{ w.url | relative_url }}"><img src="{{ w.thumbnail | relative_url }}" width="320"></a>
  <p>{{ w.status }} {{ w.price }}</p>
  <h3><a href="{{ w.url | relative_url }}">{{ w.title }}</a></h3>
  <p>{{ w.summary }}</p>
</div>
{% endfor %}
