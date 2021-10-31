## Welcome to GitHub Pages

<table>
{% tablerow me in site.data.members %}
  {{ me }}
{% endtablerow %}
</table>


### me
{% for me in site.data.members %}
- {{ me }}
{% endfor %}

### t.me
{% for t in site.data.members %}
- {{ t.me }}
{% endfor %}


<hr>
TEST
* tzst
* test2
{% assign aa = site.data.members | split: " " %}

{% for member in aa %}
* {{member}}
{% endfor %}


<hr>

 {% assign pages = site.pages | sort:"weight"  %}
<ul>
  {% for p in pages %}
    <li>
      <a {% if p.url == page.url %}class="active"{% endif %} href="{{ p.url }}">
        {{ p.title }}
      </a>
    </li>
  {% endfor %}
</ul>
