---
layout: page
title: "Home"
class: home
---

# Hi, I'm Yan Luo

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a Mphil student in the [Vislab](http://vis.cse.ust.hk/) affiliated with the Hong Kong University of Science and Technology(HKUST) under the guidance of [prof. Huamin Qu](https://seng.hkust.edu.hk/about/people/faculty/huamin-qu). Before that, I received my Bachelor’s Degree from Huazhong University of Science and Technology in Wuhan.

My interest lies in [Data Visualization](https://yanluo0913.github.io) and [Human-Computer Interaction](https://yanluo0913.github.io). I have experience in developing Visual Analytics System. Now, I'm seeking opporunity for [Data Storytelling]((https://yanluo0913.github.io)).
</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/profile.webp' type='image/webp' />
  <img
    src='/images/profile.png'
    alt='Yan Luo'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
</div>

</div>

<!-- During my first year at UW, I received support from the [Fulbright program](https://en.wikipedia.org/wiki/Fulbright_Program). In 2013, I received my B.S. from [Hasso Plattner Institute](https://hpi.de/). I am a scholar of the [German National Academic Foundation](http://www.studienstiftung.de/). I have worked with the [Open Knowledge Foundation](http://www.okfn.org), [Google Research](https://ai.google/research/), [Microsoft Research](https://www.microsoft.com/en-us/research/group/vibe/), and others. Details are in my [CV]({{ "/cv/" | relative_url }}). -->



## <a href="{{ "/publications/" | relative_url }}">Publications</a>

<div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<!-- <a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a> -->

## <a href="{{ "/projects/" | relative_url }}">Memories</a>

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>

<!-- <a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a> -->