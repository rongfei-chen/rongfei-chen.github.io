---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

I am currently a joint postdoctoral researcher at the University of Science and Technology of China (USTC) and Eastern Institute of Technology (EIT), working under the supervision of Professor Shaohua Kevin Zhou and Assistant Professor Wei Zhang.

My research investigates how embodied agents can understand human emotions and social intentions, and accordingly make socially appropriate and trustworthy decisions in interaction and collaboration. My current research interests include:

Multimodal psychological health assessment: developing multimodal frameworks for the early detection and assessment of affective disorders (e.g., depression) through the analysis of verbal and nonverbal behavioral signals;
Embodied navigation in social environments: integrating visual, auditory, and environmental semantic information to equip intelligent agents with socially aware navigation capabilities in human-centered scenarios;
Natural human–computer interaction: designing adaptive human behavior understanding and response systems with capabilities for proactive perception, empathetic interaction, and contextual adaptation.
See my [Google Scholar profile](https://scholar.google.com/citations?user=44dSBKUAAAAJ) for publications, preprints, and citation information.

<span class="anchor" id="news"></span>
# Research Updates

- Recent work on domain-specific attribute constraints in multimodal sentiment analysis: [paper](https://doi.org/10.1016/j.eswa.2026.132658) · [code](https://github.com/rongfei-chen/DSAC-EmoLLM-MSA).
- Fair multimodal sentiment analysis: [LGCDF](https://doi.org/10.3390/app16062952) · [code](https://github.com/rongfei-chen/LGCDF).
- Missing-modality research: [Evaluation Before Generation (ICME 2026, accepted)](https://arxiv.org/abs/2604.05558) · [code](https://github.com/rongfei-chen/ProMMA).

<span class="anchor" id="publications"></span>
# Publications and Preprints

The list below follows my [Google Scholar profile](https://scholar.google.com/citations?user=44dSBKUAAAAJ), checked on 8 November 2026. DOI links are provided where verified. Accepted conference papers and preprints are listed separately from published journal and conference entries. Author-confirmed updates were incorporated on 8 November 2026; alternate LLaSO titles are grouped as versions of one work.

{% assign publication_groups = "publication,accepted,preprint" | split: "," %}
{% for category in publication_groups %}
{% if category == "publication" %}
## Journal and Conference Articles
{% elsif category == "accepted" %}
## Accepted Conference Paper
{% elsif category == "preprint" %}
## Preprints
{% else %}
## Additional Manuscript
{% endif %}
{% assign papers = site.data.publications.items | where: "category", category %}
{% for paper in papers %}
<div class="publication-entry" style="margin: 0 0 1.5em 0;">
  <p style="margin-bottom: .25em;"><strong><a href="{{ paper.primary_url | escape }}">{{ paper.title | escape }}</a></strong></p>
  <p style="margin: .25em 0;">{{ paper.authors | escape }}</p>
  <p style="margin: .25em 0;">{{ paper.venue | escape }}</p>
  {% if paper.alternate_title %}<p style="margin: .25em 0; font-size: .9em; color: #667085;">Alternate version title: <a href="{{ paper.alternate_scholar_url | escape }}">{{ paper.alternate_title | escape }}</a>.</p>{% endif %}
  {% if paper.year_note %}<p style="margin: .25em 0; font-size: .9em; color: #667085;">{{ paper.year_note | escape }}</p>{% endif %}
  <p style="margin: .25em 0;"><a href="{{ paper.scholar_url | escape }}">Google Scholar record</a>{% if paper.doi %} · <a href="https://doi.org/{{ paper.doi | escape }}">DOI</a>{% endif %}{% if paper.code_url %} · <a href="{{ paper.code_url | escape }}">Code</a>{% endif %}</p>
</div>
{% endfor %}
{% endfor %}

# 🎖 Honors and Awards
- No


# 📖 Educations and Employment
- *2024.09 - 2026.09 (now)*, Working as a postdoctoral researcher at CIST, EIT. 
- *2020.09 - 2024.06*, PhD, Shanghai University.
