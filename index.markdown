---
layout: top
title: Home
section: Home
changefreq: always
link:
  - rel: canonical
    href: /
includes:
  - jquery
---
{::options parse_block_html="true" /}

![Photo of Russ Harmon](/images/russ_harmon.jpg){: width="150" .inset .right }

Welcome
=======

I'm Russ Harmon, a <span id="age">twenty seven or so</span> year old programmer
currently located in San Francisco, CA.  What you see below is some ramblings by
me about myself or other things.

<script type="text/javascript">
  $("#age").replaceWith(
    new Number(
        Math.floor(
          (new Date() - new Date("{{ site.birthdate }}"))
            / 31556926000 /* nanos per year */)).toWords());
</script>

<div class="section">
# Academics
I completed my studies at the [Rochester Institute of Technology][RIT] in
December, 2013. My thesis can be found [here][ruminate-thesis].
</div>

<div class="section">
# Code

The largest piece of publicly released work I've done is the code for my thesis
which resulted in [Ruminate], an introspective library for C.

The vast majority of my other work can be found at my [GitHub] page.
What you can see below is the five most recent projects I've worked on at
GitHub.

<div id="github_{{ site.github_username }}">
Contacting GitHub...
{: #github_loading .loading }
<ul class="compact recent" id="github_list"/>
</div>
</div>

<div class="section">
# Blog
I periodically post to a programming blog entitled
_[Machinae Elegantiam](/machinae)_.

{% for post in site.categories.machinae limit: 3 %}
* [{{ post.title }}]({{ post.url }}){: title="{{ post.excerpt | strip_html | truncatewords: 20 }}"}
{: .compact .recent }
{% endfor %}
</div>

[Ruminate]: /ruminate
[ruminate-thesis]: /files/project-report.pdf
[RIT]: http://www.rit.edu/
[GitHub]: https://github.com/eatnumber1

{% comment %}
vim: ft=liquid sw=4 ts=4 sts=4 tw=80 noet
{% endcomment %}
