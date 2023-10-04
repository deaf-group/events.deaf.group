---
layout: page
title: 📃 Event List
permalink: list
---
<button id="resetButton">Reset All</button>
{% include filter-year-list.html %}
{% include filter-country-list.html %}
<ui id="eventList">
    {% for event in site.events %}
        <li data-country="{{event.event_country}}" data-date="{{event.event_date}}">{{event.event_country}}, {{event.event_region}} - <a href="{{event.url}}">{{event.title}} {{event.event_date}}</a>
    </li>
    {% endfor %}
</ui>
{% include filter.html %}