---
title: DriveNow Affiliate widget demo site
---
{% assign groups = site.pages | group_by: 'layout' | sort: 'title' %}
{% for group in groups %}
## {{ group.name }}
		{% for page in group.items %}
			{% if page.layout == 'dev' or page.layout == 'staging' or page.layout == 'production' %}
* <a href="{{ page.url | relative_url  }}">{{ page.title }}</a>
			{% endif %}
		{% endfor %}
{% endfor %}
