---
layout: post
title: Materials
cover: readings.jpg
categories: posts
permalink: materials
tag: hei
year: 2022
---
Here you will find papers, vignettes, and other resources mentioned in the class. They will be added as the course progresses.



## Vignettes
<a href="https://www.youtube.com/channel/UCnYEe45w6F4G3AEYCyNHMWg/videos" target="_blank">{{"PBOC Youtube channel"}}</a>
This series of vignettes expands on topics we will cover in the course. Specific suggestions for vignettes to watch will be given during the course.

<table>
<tr>
    <th style="width:130px"><b>Date</b></th>
    <th><b>Topic</b></th>
</tr>
{% for day in site.data.vignettes %}
{% if day.exurl %}
{% else %}
<tr>
    <td>{{day.date}}  </td>
    <td>{{day.topic1}}
    {% if day.videos1 %}
    {% for v in day.videos1 %}
    {% if v.name %}
    <a href="http://rpdata.caltech.edu/courses/aph161/2021/videos/{{v.name}}" target="_blank">{{v.title}}</a><br/>
    {% else %} 
    <a href="{{v.url}}" target="_blank">{{v.title}}</a><br/>
    {{v.description}}<br/>
    {%endif %}
    {%endfor%}
    {%endif %}
    {{day.topic2}}
    {% if day.videos2 %}
    {% for v in day.videos2 %}
    {% if v.name %}
    <a href="http://rpdata.caltech.edu/courses/aph161/2021/videos/{{v.name}}" target="_blank">{{v.titlea}}</a><br/>
    {% else %}
    <a href="{{v.urla}}" target="_blank">{{v.titlea}}</a><br/>
    {{v.descriptiona}}<br/>
    {%endif %}
    {%endfor%}
    {%endif %}
    </td>
    <!--<td>--->
    <!--{% if day.slide %}--->
    <!--<a href="http://rpdata.caltech.edu/courses/aph161/protected/2022/slides/{{day.slide}}">Slides</a>--->
    <!--{%endif%}---> 
    <!--</td>---> 

  <!-- {% if day.slide %} 
  <td>
  {% for s in day.slide %}
  <a href="http://rpdata.caltech.edu/courses/aph161/protected/2020/videos/{{s}}"><b class="post-title">{{s}}</b></a> 
  {%endfor%}
  </td>
  {% else %}
  <td> {{'-'}} </td>
  {% endif %} -->
</tr>
{% endif %}
{% endfor %}
</table>


## In-Class Readings

{% assign readings = site.data.papers %}

{% for week in readings %}
<span style="display: block; font-weight: 500"> <b>{{ week[0] }}</b></span>

{% for p in week[1] %}
{% assign dir = "http://rpdata.caltech.edu/courses/course_papers/protected/" %}
{% if p.link != None %}
{% assign dir = p.link %}
{% if p.journal != None %}
<a href="{{p.link}}" target="_blank">{{p.title}}</a> by {{ p.author }} *{{ p.journal }}* {{ p.volume }}{{ p.number }} {{ p.year }}. {{ p.description }}
{% else %}
<a href="{{p.link}}" target="_blank">{{p.title}}</a> by {{ p.author }}{{ p.volume }}{{ p.number }}{{ p.year }}. {{ p.description }}
{% endif %}
{% elsif p.PDF != None %}
[{{ p.title }}]({{ dir }}{{ p.PDF }}) by {{ p.author }} *{{ p.journal }}* {{ p.volume }}{{ p.number }} {{ p.year }}. {{ p.description }}
{% else %}
{{p.title}} by {{ p.author }} *{{ p.journal }}* {{ p.volume }}{{ p.number }} {{ p.year }}. {{ p.description }}
{% endif %}
{% endfor %}
{% endfor %}


## miscellaneous

<a href="http://rpdata.caltech.edu/courses/heidelberg_22/open_data/Kondev_course_notes.pdf" target="_blank">{{"Jane's notes -- stat mech and diffusion"}}</a><br>

<a href="http://rpdata.caltech.edu/courses/heidelberg_22/open_data/Kondev_course_notes_poisson.pdf" target="_blank">{{"Jane's notes -- poisson distribution"}}</a><br>

Here are links to homeworks involving order of magnitude estimates: <a href="http://www.rpgroup.caltech.edu/aph161/assets/hwk/HW_1_161_2022_Final.pdf" target="_blank">{{"BE161: Homework 1"}}</a>, <a href="http://www.rpgroup.caltech.edu/aph161/assets/hwk/HW_2_161_2022_Final.pdf" target="_blank">{{"BE161: Homework 2"}}</a>. <br>

<a href="https://improbable.com/2019/03/29/the-day-ig-nobel-people-came-together-at-hokkaido-university/?amp=1" target ="_blank">{{"The ignoble prize"}}</a>
