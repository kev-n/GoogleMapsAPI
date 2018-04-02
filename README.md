# JSCRIPT 200 Winter 2018 Final Project

**Google Maps API | Infinite Ajax Scroll | JQuery**

- Google Maps with autocomplete, directions, search, and rotating satellite view.
- Infinite AJAX Scroll JQuery plugin enables the page to load when scrolled to bottom.
- Collapsible left-sticky navigation menu with JQuery.

## [Google Maps API](https://developers.google.com/maps/)

- Please replace with your own API key.
- To obtain a Google Maps API key:
   1. Go to the [Google API Console](https://console.developers.google.com/flows/enableapi?apiid=maps_backend,geocoding_backend,directions_backend,distance_matrix_backend,elevation_backend,places_backend&reusekey=true).
   2. Create or select a project.
   3. Click **Continue** to enable the API and any related services.
   4. On the **Credentials** page, get an **API key** (and set the API key restrictions).
 
 ## [Infinite AJAX Scroll](https://infiniteajaxscroll.com/)
 
 - Extensible through extensions.
 - Quick and easy to implement because it extends your already existing server-side pagination (takes less then 5 minutes to implement).
 - Infinite AJAX Scroll is open source and is available on [GitHub](https://github.com/webcreate/infinite-ajax-scroll)
 > Progressive enhancement: Infinite AJAX Scroll works by enhancing your server-side pagination with AJAX. When a client doesn't support JavaScript it will fall back on your server-side pagination.
 > [Infinite Ajax Scroll](https://github.com/webcreate/infinite-ajax-scroll)
 
 Markup:
 ```html
 <div class="container">
  <div class="item">...</div>
  <div class="item">...</div>
</div>

<div id="pagination">
  <a href="page1.html">1</a>
  <a href="page2.html" class="next">2</a>
</div>
 ```
 
 Javascript:
 ```javascript
 var ias = $.ias({
  container:  ".container",
  item:       ".item",
  pagination: "#pagination",
  next:       ".next a"
});

ias.extension(new IASSpinnerExtension());            // shows a spinner (a.k.a. loader)
ias.extension(new IASTriggerExtension({offset: 3})); // shows a trigger after page 3
ias.extension(new IASNoneLeftExtension({
  text: 'There are no more pages left to load.'      // override text when no pages left
}));
 ```
 ## [JQquery](http://jquery.com/)
 
 - Please remember to link to your *JQuery* file or use the [Google Hosted Jquery](https://developers.google.com/speed/libraries/#jquery):
 
 ```
 <head>
   <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
 </head>
 ```
 