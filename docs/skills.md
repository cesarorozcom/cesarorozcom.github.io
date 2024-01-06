---
layout: default
title: Skills
---
[back](./)

## Skills

---

<div class="container-fluid">
{% if site.data.skills %}
{% assign skills = site.data.skills%}

{% for item in skills%}
 {% assign parent_key = item | first %}
<br>
<div class="row align-items-start">
 
 <div class="col-md-12">
  <span><h3>{{ parent_key }}</h3></span>
 </div>
</div>

 {% for i in skills[parent_key] %} 
  <div class="row">
     <div class="col">
      <p class="text-secondary"><h5> {{ i.name }}</h5> </p>
     </div>
  </div>
  <div class="row">
    {% for it in i.items %}
     <div class="col">
       {{ it }}
     </div>
    {% endfor %}
  </div>

 {% endfor %}


{% endfor %}
{% else %}
<h3>Ups! No skill file found.</h3>
{% endif %}

</div>