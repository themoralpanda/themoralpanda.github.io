---
title: Blog
date: 2021-09-07T14:15:35+05:30
---

---

<section id="conten"t>
  <h4> Blog </h4>
  <ul class=posts_listing>
    {{ range .Site.RegularPages.ByPublishDate.Reverse }}
      <div id="posts">
        {{if not (in .Params.tags "disable")}}
        <div id=date class="date-time-title" style="font-size:0.7em">
            <time>{{ .Date.Format (.Site.Params.dateform | default "Jan 02 2006") }}</time>
        </div>
        <div class="date-time-title post" style="font-size:0.9em">
          <a href="{{ .Permalink }}">{{ .Title }}</a>
        </div>
        {{end}}
      </div>
    {{ end }}
  </ul>
</section>