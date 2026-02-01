<h2 id="publications" style="margin: 2px 0px 20px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li style="margin-bottom: 30px;">
  <div class="pub-row">
    <div class="col-sm-9" style="position: relative; width: 100%;">
      {% if link.conference_short %} 
      <span class="badge" style="margin-bottom: 8px; display: inline-block;">{{ link.conference_short }}</span>
      {% endif %}
      <div class="title" style="margin-bottom: 8px; line-height: 1.4;"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author" style="margin-bottom: 6px;">{{ link.authors | replace: "Zhuoyan Li", "<strong>Zhuoyan Li</strong>" }}</div>
      <div class="periodical" style="margin-bottom: 8px;"><em>{{ link.conference }}</em></div>
      {% if link.notes %} 
      <div style="margin-bottom: 8px;"><strong><i style="color:#e74d3c">{{ link.notes }}</i></strong></div>
      {% endif %}
      <div class="links">
        {% if link.pdf %} 
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
        {% endif %}
        {% if link.code %} 
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
        {% endif %}
        {% if link.page %} 
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
        {% endif %}
        {% if link.bibtex %} 
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
        {% endif %}
        {% if link.others %} 
        {{ link.others }}
        {% endif %}
      </div>
    </div>
  </div>
</li>

{% endfor %}

</ol>
</div>

