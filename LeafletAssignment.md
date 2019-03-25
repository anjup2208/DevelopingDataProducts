---
title: "Developing Data Products - Maps"
author: "Anju Mandal"
date: "March 25, 2019"
output: 
  html_document:
    keep_md: true
---

### Some Hertiage sites in India 


```r
   library(leaflet)
```

```
## Warning: package 'leaflet' was built under R version 3.5.3
```

```r
   HertiageSites <- data.frame(
       lat = c(27.1750,28.6562,19.8876,9.9195,17.3616),
       lng = c(78.0422,77.2410,86.0945,78.1193,78.4747)
   )
   links <- c("<a href=https://www.tajmahal.gov.in/> Taj Mahal</a>",
              "<a href=http://asi.nic.in/red-fort-delhi/> Red Fort</a>",
              "<a href=http://www.konark.nic.in/>Sun Temple</a>",
              "<a href=www.maduraimeenakshi.org/>Meenakshi Temple</a>",
              "<a href=https://telanganatourism.gov.in/partials/destinations/heritage-spots/hyderabad/charminar.html
                >Charminar</a>"
              )
   
   HertiageSites %>%
       leaflet() %>%
       addTiles() %>%
       addMarkers(popup = links)
```

<!--html_preserve--><div id="htmlwidget-e4289a2b4d6b56ed3482" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-e4289a2b4d6b56ed3482">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addMarkers","args":[[27.175,28.6562,19.8876,9.9195,17.3616],[78.0422,77.241,86.0945,78.1193,78.4747],null,null,null,{"interactive":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},["<a href=https://www.tajmahal.gov.in/> Taj Mahal<\/a>","<a href=http://asi.nic.in/red-fort-delhi/> Red Fort<\/a>","<a href=http://www.konark.nic.in/>Sun Temple<\/a>","<a href=www.maduraimeenakshi.org/>Meenakshi Temple<\/a>","<a href=https://telanganatourism.gov.in/partials/destinations/heritage-spots/hyderabad/charminar.html\n                >Charminar<\/a>"],null,null,null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]}],"limits":{"lat":[9.9195,28.6562],"lng":[77.241,86.0945]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->
