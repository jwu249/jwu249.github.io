---
name: Assignment 6 Visualizations - Big Foot Data Set
tools: [Python, HTML, vega-lite, altair]
image: assets/pngs/altair_viz1.png
description: Creating interactive visualization with Altair and Vega-lite on a inclass dataset
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
---

# Assignment 6 Visualizations
-------------------------------------------------------------
## Big Foot Sightings Visualization
This visualization uses Vega-Lite and Altair to create an interactive chart(Select an area over the map).

<div id="vega-chart" style="width: 100%;"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>
<script>
  vegaEmbed("#vega-chart", "{{ site.baseurl }}/assets/json/test.json")
    .then(function(result) {
      console.log("Vega chart rendered successfully");
    })
    .catch(console.error);
</script>

The plot helps people visualize the Big Foot sightings in the USA while built into the visualization is a select cursor to highlight a specific area of the map which will highlight the visibility scores of those sightings. In this plot, it is similar to the plot I had done in Homework 5 but I just changed the interactivity instead of a slider, I went with the selector.

#### Design:
In the design of this page, I wanted a visual that is easy to understand but incorporates elements of data on a map where people can visually see where people have supposely seen Big Foot. I went with Quantitative data as I was able to map the longitude and latitude onto the map. Additionally, I chose the cool steel color to color the points instead to visually contrast the map. 

## Seasons and UV Index Chart
<div id="uv-index-chart" style="width: 100%;"></div>

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script>
  // Embed the chart
  vegaEmbed("#uv-index-chart", "{{ site.baseurl }}/assets/json/big_foot_data_2.json")
    .then(function(result) {
      console.log("UV Index chart rendered successfully");
    })
    .catch(console.error);
</script>

The next plot I decided to do was just to visualize the UV indexes in each season to allow people to make their own inference according to the first plot as the UV index can also play into the visibility of Big Foot. I believe the data is representative of the UV indexes in each season and I decided to leave the null information because it is representative of the amount of data that didn't keep track of the index which can play into the validity of the sightings or they just didn't know.

#### Design:
I went with a bar chart because it is visually comparable and viewers to visualize the UV Indexes of the data according to the seasons.

## Search The Data & Methods

Below are links to the data and analysis code:

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="Big_Foot Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jwu249/jwu249.github.io/blob/main/python_notebooks/altair_viz.ipynb" text="The Analysis" %}
</div>
