---
layout: page
permalink: /publications/
title: publications
description:  
years: [2024, 2023, 2022, 2021, 2020]
nav: true
nav_order: 1
---

<div class="publications">

<h2 class="year">preprints</h2>
{% bibliography -f papers -q @*[preprint=true]* %}

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}} && preprint!=true]* %}
{% endfor %}

</div>