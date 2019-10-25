---
layout: page
title: Adventures
permalink: /adventures/
description: A growing collection of your cool adventures.
---

{% for adventure in site.adventures %}

{% if adventure.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ adventure.redirect }}" target="_blank">
        {% if adventure.img %}
        <img class="thumbnail" src="{{ adventure.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ adventure.title }}</h1>
            <br/>
            <p>{{ adventure.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ adventure.url | prepend: site.baseurl | prepend: site.url }}">
        {% if adventure.img %}
        <img class="thumbnail" src="{{ adventure.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ adventure.title }}</h1>
            <br/>
            <p>{{ adventure.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
