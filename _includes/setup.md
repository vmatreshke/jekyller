{% capture strip_whitespace %}
{% capture theme %}{% if page.theme %}{{ page.theme }}{% else %}{{ site.default_theme }}{% endif %}{% endcapture %}
{% capture lang %}{% if page.lang %}{{ page.lang }}{% else %}{{ site.default_lang }}{% endif %}{% endcapture %}
{% capture body_class %}{% if page.body_class %}{{ page.body_class }}{% else %}{{ site.default_body_class }}{% endif %}{% endcapture %}

{% capture author_name %}{% if page.author %}{% if page.author.name %}{{ page.author.name }}{% else %}{{ page.author }}{% endif %}{% else %}{{ site.author.name }}{% endif %}{% endcapture %}
{% capture author_url  %}{% if page.author %}{{ page.author.url }}{% else %}{{ site.author.url }}{% endif %}{% endcapture %}

{% capture company_name %}{% if page.author.company %}{% if page.author.company.name %}{{ page.author.company.name }}{% else %}{{ page.author.company }}{% endif %}{% elsif page.company %}{% if page.company.name %}{{ page.company.name }}{% else %}{{ page.company }}{% endif %}{% else %}{{ site.author.company.name }}{% endif %}{% endcapture %}
{% capture company_url  %}{% if page.author.company %}{{ page.author.company.url }}{% elsif page.company %}{{ page.company.url }}{% else %}{{ site.author.company.url }}{% endif %}{% endcapture %}

{% capture title %}{% if page.title %}{{ page.title }}{% else %}{{ supertitle }}{% endif %}{% endcapture %}

{% capture subtitle %}{% if page.subtitle %}{{ page.subtitle }}{% else %}{% if author_url != '' %}[{{ author_name }}]({{ author_url }}){% else %}{{ author_name }}{% endif %}{% if company_name %}, {% if company_url != '' %}[{{ company_name }}]({{ company_url }}){% else %}{{ company_name }}{% endif %}{% endif %}{% endif %}{% endcapture %}{% capture subtitle %}{{ subtitle | markdownify }}{% endcapture %}

{% capture fork_url %}{% if page.fork_url %}{{ page.fork_url }}{% else %}{{ site.fork_url }}{% endif %}{% endcapture %}
{% capture progress %}{% if page.progress %}{{ page.progress }}{% else %}{{ site.progress }}{% endif %}{% endcapture %}
{% endcapture %}
