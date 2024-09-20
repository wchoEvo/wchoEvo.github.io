---
title: "Members"
layout: default
excerpt: "Members"
sitemap: false
permalink: /members/
---

<h1>{{page.title}}</h1>

<!-- Members -->

<h2><a id="members"></a>Members</h2>
{% assign members = site.posts | where: 'category', 'current' | sort: 'date' %}
{% for member in members %}
<div class="card team-member-card">
    <div class="row mt-3">
        <div class="col-md-2">
            <a href={{member.url}}>
                <img src="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.image }}"
                    class="card-img img-responsive img-thumbnail"
                    style="filter: grayscale(100%); max-width: 100px;"/>
            </a>
        </div>

        <div class="col-md-10">
            <div class="card-body">
            <h4 class="card-title">{{ member.title }}</h4>
            <p class="card-text">{{ member.role }}</p>
            </div>
        </div>
    </div>
</div>
{% endfor %}

<!-- Alumni -->

<h2><a id="alumni"></a>Alumni</h2>
{% assign members = site.posts | where: 'category', 'alumni' | sort: 'date' %}
{% for member in members %}
<div class="card team-member-card">
    <div class="row mt-3">
        <div class="col-md-2">
            <a href={{member.url}}>
                <img src="{{ site.url }}{{ site.baseurl }}/images/team/{{ member.image }}"
                    class="card-img img-responsive img-thumbnail"
                    style="filter: grayscale(100%); max-width: 100px;"/>
            </a>
        </div>

        <div class="col-md-10">
            <div class="card-body">
            <h4 class="card-title">{{ member.title }}</h4>
            <p class="card-text">{{ member.role }}</p>
            </div>
        </div>
    </div>
</div>

{% endfor %}

[comment]: # (The design is based on https://www.allanlab.org/aboutwebsite.html)
