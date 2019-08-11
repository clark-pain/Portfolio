<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  {% if site.owner.google.verify %}<meta name="google-site-verification" content="{{ site.owner.google.verify }}">{% endif %}
  {% if site.owner.bing-verify %}<meta name="msvalidate.01" content="{{ site.owner.bing-verify }}">{% endif %}

  {% if site.plugins contains 'jekyll-seo-tag' or site.gems contains 'jekyll-seo-tag' %}
    {% comment %}
      Add metadata for search engines and social networks if jekyll-seo-tag plugin is enabled
    {% endcomment %}
    {% include head-seo.html %}
  {% else %}
    <title>{% if page.title %}{{ page.title | escape }}{% else %}{{ site.title | escape }}{% endif %}</title>
    <meta name="description" content="{{ page.excerpt | default: site.description | strip_html | normalize_whitespace | truncate: 160 | escape }}">
    <link rel="canonical" href="{{ page.url | replace:'index.html', '' | absolute_url }}">
  {% endif %}

  <script>
    /* Cut the mustard */
    if ( 'querySelector' in document && 'addEventListener' in window ) {
      document.documentElement.className = document.documentElement.className.replace(/\bno-js\b/g, '') + 'js';
    }
  </script>

  <link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}">
  {% if site.google_fonts %}
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family={%- for font in site.google_fonts -%}{{ font.name | replace: ' ', '+' }}{% if font.weights %}:{% endif %}{{ font.weights | remove: ' ' }}{% if forloop.last != true %}|{% endif %}{%- endfor -%}">
  {% endif %}

  {%- if site.plugins contains 'jekyll-feed' or site.gems contains 'jekyll-feed' -%}
    {%- comment -%}
      Add Atom feed link if jekyll-feed plugin is enabled
    {%- endcomment -%}
    {% include head-feed.html %}
  {%- endif -%}

  {%- if site.head_scripts -%}
    {%- for script in site.head_scripts -%}
      {%- if script contains "://" -%}
        {%- capture script_path %}{{ script }}{% endcapture -%}
      {%- else -%}
        {%- capture script_path %}{{ script | absolute_url }}{% endcapture -%}
      {%- endif -%}
      <script src="{{ script_path }}"></script>
    {%- endfor -%}
  {%- endif -%}

  {% include head-custom.html %}
</head>

title: "Hi, I'm Clark"
image: 
  path: /docs/Banner.jpg
  thumbnail: /docs/Banner.jpg
  caption: "Photo from [WeGraphics]"
categories:
  - Layout
tags:
  - content
  - image
  - layout
last_modified_at: 2018-01-31T14:28:50-05:00
---

This post should display a large hero image at the top of a page.

This post tests a horizontal image using the following YAML Front Matter:

```yaml
image:
  path: /images/eder-oliveira-180877.jpg
```

Hero images can also be assigned more succinctly when `thumbnail` or `caption` are not used.

```yaml
image: /images/eder-oliveira-180877.jpg
```

Tall images will push content down the page. `1600 x 600` is a good middle-ground size to aim for.

## Clark: Professional, Sun lover, Jokester

Welcome to my portfolio. Included is information regarding my professional experience, skills, and personal interests.

I believe that every complex problem has an elegant and efficient solution. I am not one to cut corners or sacrifice quality for the sake of convenience. 

### Bio
Hometown, hobbies, how i got to where i am now

### What am I doing
Air Force intelligence officer, space systems experience 

### 



### Interests

  - Process improvement
  - Outdoors 
  - Athletics
  - Conservation
  - Entrepreneurism 
  - Working for posterity 

### What I Can Do For You

  - Taclke tough problems head-first 
  - 

#### Contact Me 
Email <clark.pain@gmail.com>

---
