---
layout: layouts/home.njk
title: Against the Grain - London Cider
permalink: /
navtitle: Home
strapline: "Inspired cider for London"
menu: [
  {
    "id": "header",
    "title": "Home"
  },
  {
    "id": "ciders",
    "title": "Ciders"
  },
  {
    "id": "story",
    "title": "Story"
  }
]
ciders: [
  {
    "classname":  "laid-back-lumberjack",
    "image": "laid-back-lumberjack-product-image-against-the-grain.png",
    "imageAlt": "Laid-back Lumberjack",
    "title": "Laid-back <br />Lumberjack",
    "subtitle": "Original session <br />cider",
    "info": "4.1% ABV",
    "description": "Medium dry apple cider, <strong>bright gold</strong> colour. <strong>Full bodied</strong> and deep, clear cider with just a <strong>hint of sweetness</strong>.",
    "smallprint": "<strong><small>Available in:</small> <br />30L Dolium Keg (Sankey S- type)</strong>"
  },
  {
    "classname": "gypsys-kiss",
    "image": "gypsys-kiss-product-image-against-the-grain.png",
    "imageAlt": "Gypsy’s Kiss logo",
    "title": "Gypsy’s <br />Kiss",
    "subtitle": "Dry hopped <br />cider",
    "info": "5.0% ABV",
    "description": "Dry-hopped cider, <strong>golden colour</strong>. Complex cider dry-hopped with Crystal hops, adding <strong>piney, floral and spicy</strong> notes.",
    "smallprint": "<strong><small>Available in:</small> <br />30L Dolium Keg (Sankey S- type)</strong>"
  },
  {
    "classname": "hippie-tripper",
    "image": "hippie-tripper-product-image-against-the-grain.png",
    "imageAlt": "Hippie Tripper logo",
    "title": "Hippie <br />Tripper",
    "subtitle": "Cherry and <br />Pomegranate cider",
    "info": "4.0% ABV",
    "description": "<strong>Medium fruited</strong> cider, light pink colour. Light and sparkling, with delicious <strong>fruity overtones</strong>.",
    "smallprint": "<strong><small>Available in:</small> <br />30L Dolium Keg (Sankey S- type)</strong>"
  },
]
storyStrapline: "Our Story"
storyContent: "<p>Jono’s love for brewing and cider making goes back over a decade, with three years’ experience following his passion as a professional brewer.</p><p>However, his West Country roots, and the lack of interesting cider in London, drove him to pack-in the grain and strike out on his own.</p><p>Well, not on his own.</p><p>Conor comes from an entrepreneurial background working within the catering industry and, over quite a few pints with Jono, got pretty excited about changing the face of London’s cider.</p><p>After the hangover, they teamed up to create Against The Grain, a micro-cidery based in South West London. Crafting exciting and innovative new-age ciders, they aim to propel the world of cider to new heights.</p>"
bannerStrapline: "See&nbsp;it. Taste&nbsp;it. Stock&nbsp;it. <br />Tell&nbsp;everyone about&nbsp;it."
email: "jono@againstthegraincidery.co.uk"
address: "25 Summerstown<br />London, SW17 0BQ"
telephone: "07411 847 663"
socialLinks: [
  {
    "url": "https://www.facebook.com/AgainstTheGrainCidery/",
    "title": "Facebook"
  },
  {
    "url": "https://www.instagram.com/againstthegraincidery/",
    "title": "Instagram"
  },
  {
    "url": "https://twitter.com/ATGcidery",
    "title": "Twitter"
  }
]
copyright: "© Against the Grain 2019"
---

<header id="header" class="header">
  <h1 class="header__title"><span class="screen-reader-text">{{title}}</span></h1>
  <nav class="header__nav">
  <ul>
  {% for item in menu %}
  <li><a href="#{{item.id}}" class="js-scroll-to">{{item.title}}</a></li>
  {% endfor %}
  </ul>
  </nav>
</header>

<section class="banner banner--intro">
  <div class="banner--intro__clouds--1"></div>
  <div class="banner--intro__clouds--2"></div>
  <div class="bg banner--intro__landscape"></div>
  <div class="banner--intro__barrel"></div>
  <div class="banner__content">
    <h2 class="strapline stroked">{{strapline}}</h2>
  </div>
</section>

<section class="ciders" id="ciders">
<ul class="ciders__list">
{% for cider in ciders %}
  <li class="ciders__list-product ciders__list-product--{{cider.classname}}">
  <div class="ciders__list-image"><img width="600" height="600" src="static/img/{{cider.image}}" alt="{{cider.title}} logo" /></div>
  <h3 class="ciders__list-title stroked">{{cider.title}}</h3>
  <h4 class="ciders__list-subtitle">{{cider.subtitle}}</h4>
  <h4 class="ciders__list-subtitle">{{cider.info}}</h4>
  <p class="ciders__description">{{cider.description}}</p>
  <p>{{cider.smallprint}}</p>
</li>
{% endfor %}
</ul>
</section>

<section id="story" class="banner banner--our-story">
  <div class="banner__content banner__content--fixed">
  <h2 class="strapline">{{storyStrapline}}</h2>
  {{storyContent}}
  </div>
</section>

<section class="banner banner--strapline">
  <div class="banner__content">
      <h2 class="strapline stroked">{{bannerStrapline}}</h2>
  </div>
</section>

<footer id="footer" class="footer">
  <div class="footer__contact">
    <h3 class="footer__title"><strong><a href="mailto:{{email}}">Stock us</a></strong></h3>
    <p>
      <strong>Contact us:</strong><br />
      {{address}}
    </p>
    <p>
      <strong>Tel:</strong> {{telephone}}<br />
      <strong>Email:</strong> <a href="mailto:{{email}}">{{email}}</a>
    </p>
  </div>
  <div class="footer__links">
    <nav class="social-links">
<ul>
{% for item in socialLinks %}
<li><a href="{{item.url}}" target="_blank"><span class="screen-reader-text">{{item.title}}</span></a></li>
{% endfor %}
</ul>
    </nav>
  </div>
  <p class="footer__copyright">{{copyright}}</p>
</footer>
