#Drupal + Angular

### Introduction
For a *private* Drupal project, there is a need of a dynamic dashboard, which will have different Views / Panes in it, and those have to be dynamic, entities created fast, updated almost instant, all based on ajax and with no page reloads. Panes should be able to collapse / expand on the flight and small entities (which we've decided that won't be full pages) should have an instant preview. All of those are just a part of a Drupal project, there of course are pages which won't have such dynamic elements, most of the user profiles will just be simple cached pages, login screens, etc.

So this is how the idea of Drupal + Angular came to life. Of course there are other modules out there that get the job done. In my case, I thought to **make a strong and dynamic integration with angular** (drop and cut as much as we can from Drupal, maybe put htaccess in predefined folders of any module that defines partials there, etc.), **make a good integration with Services / RESTful module** (automatically provide all the bundles, taxonomies, etc. as *services* in Angular, so we won't have to define those manually) and **make a standard of creating angular apps as Custom Ctools Contents** (so that we can drop them in any panel we want).

---

*Okay, so more I thought about it, it would be nice to have 3 different modules:*

* **Angular API** - this offers AngularJS integration, libraries (CDN, Production, etc.), different useful tools and functions.

  Project URL: https://github.com/Nikro/drupal-angular-api

* **Angular REST** - this offers a link between AngularJS and Services RESTful module. Basically just a consumption of services by $resource, but it would be awesome if we offer extra resources, specifically PER bundle, comment bundle, taxonomy bundle (term in voc), also write-up JS that automatically offers those services dynamically to be available.

  Project URL: https://github.com/Nikro/drupal-angular-restful 

* **Angular Ctools** - this offers a link between AngularJS & Ctools. I was thinking a lot about this module, it can’t offer a custom content-type, because those will be basically offered by custom modules themselves. What it can offer, is some helper tools for easier work with AngularJS Apps and Controllers in the context of Ctools / Panels.

  Project URL: https://github.com/Nikro/drupal-angular-ctools
