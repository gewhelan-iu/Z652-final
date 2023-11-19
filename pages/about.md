---
title: About
layout: about
permalink: /about.html
# include CollectionBuilder info at bottom
credits: true
# Edit the markdown on in this file to describe your collection
# Look in _includes/feature for options to easily add features to the page
---

{% include feature/jumbotron.html objectid="https://cdil.lib.uidaho.edu/images/palouse_sm.jpg" %}

{% include feature/nav-menu.html sections="About the Collection;About the About Page" %}

## About the Collection
The primary purpose of this digital collection is to catalog the bookmarks that my family has purchased at various tourist sites in the United Kingdom. With that goal in mind, the information gathered from the items themselves will be fairly comprehensive, including all text and illustrations, color, and dimensions. Beyond that, information regarding the physical event of the visit to each location will also be presented, including geographic and administrative location, and where possible, the year in which the visit occurred and a photo of the site taken at that time. In order to keep the bookmarks as the focal point of the collection, Collection Builder's "multiple" item feature will be used to present each bookmark as a main entry, with the other images being secondary items. Furthermore, access points based on the administrative location (using the United Kingdom's official region list) will be used, to enable a visualization of which parts of Great Britain my family has spent the most time in.  
The collection will be searchable by title, text, location, and date, and sortable by name and date. The expected use of this collection will be by people who are familiar with my family's travels, British tourist sites, or both, and as such these are the fields which are most likely to be used for searching. Furthermore, the remainder of the fields have data which is either not sufficiently controlled or is numerical and therefore less intuitive for the average user (excepting year). Filtering by date, primary color, location, the presence of images on the bookmark, and the presence of supporting images will also be available. Some of these filters are of further assistance to searchers, while others will serve as a rudimentary way of analyzing the collection as a whole, by, for example, displaying the relative frequency of primary colors.  
Below are two tables which provide guidance on the creation of item metadata for this creation. The first table is for main entries, which will carry all of the textual metadata about each bookmark and site. The second table is for child items, which will be the images themselves. These child items will have minimal descriptive metadata of their own, because they will be presented alongside the main entry metadata. 
## Metadata
### For main entries: 
 
|Field|Description|Obligation|Cardinality|DC Equivalency|Example|
|---|---|---|---|---|---|
|objectid|Unique identifier of object. Use distinctive word or words from title, with prefix `mt_` for main entries.|Required|1|IdHientifier|mt_warwick|
|filename|Name of file. Use distinctive word or words from title, with prefix `bm_` for bookmark files.|Required|1|Identifier|bm_warwick.png|
|format|Format of collection item. Use `multiple`.|Required|1|Format|multiple|
|title|Site which the bookmark commemorates. Transcribe exactly. Capitalize only proper nouns.|Required|1|Title|Warwick Castle|
|text|All non-title text present on the bookmark. Transcribe exactly. Capitalize only proper nouns. When there are multiple areas of text, separate contiguous sections with space, semicolon, space.|Required when present|0+|Description|Cæsar's Tower ; the Great Hall ; Great Curtain Wall|
|description|Brief, one-sentence descriptions of any illustrations on the bookmark. When there are multiple illustrations, separate each description with space, semicolon, space.|Required when present|0+|Description|Cæsar's Tower, with the castle wall in the background and greenery in the foreground ; Large hall with a ribbed ceiling, a large painting, and suits of armor in ogive stands ; The castle's curtain wall, with the gatehouse on the left and Guy's Tower on the right.|
|latitude|Latitude of site, to 5 decimal places. For locations larger than a single building, use the coordinates of the site's Google Maps entry.|Required|1|Coverage|52.27947|
|longitude|Longitude of site, to 5 decimal places. For locations larger than a single building, use the coordinates of the site's Google Maps entry.|Required|1|Coverage|-1.58745|
|location|Region of site. Use [official list of English regions](https://www.ons.gov.uk/methodology/geography/ukgeographies/administrativegeography/england) for locations in England, and "Wales" or "Scotland" for sites in those countries.|Required|1|Location|West Midlands|
|image|Representative image of site from private collection. For main entries only.|Optional|0-1|Relation|warwick.jpg|
|date|Year of acquisition of bookmark.|Optional|1|Date|1994|
|color|Color of leather and illustrations. Format as `<primary>,<secondary>`.|Required|2|Description|blue,gold|
|dimensions|Length and width of bookmark, in centimeters, to one decimal place. Format as `<length>cmx<width>cm`.|Required|1|Description|22.9cmx4.1cm|

### For child items:

|Field|Description|Obligation|Cardinality|DC Equivalency|Example|
|---|---|---|---|---|---|
|objectid|Unique identifier of object. Use distinctive word or words from title, with prefix `bm_` for bookmark entries and no prefix for accompanying image entries.|Required|1|Identifier|bm_warwick|
|filename|Name of file. Use distinctive word or words from title, with prefix `bm_` for bookmark files and no prefix for accompanying image files.|Required|1|Identifier|bm_warwick.png|
|format|Format of image.|Required|1|Format|multiple/png|
|parentid|Object ID of parent items in pairs.|Required|0-1|Relation|bm_warwick|
|title|Site which the bookmark commemorates. Transcribe exactly. Capitalize only proper nouns.|Required|1|Title|Warwick Castle|

## About the Site

This site is generated using [CollectionBuilder-GH](https://collectionbuilding.github.io/gh/), a project to create a free and simple digital collection using [GitHub Pages](https://pages.github.com/) from: 

- a CSV of collection metadata
- a folder of JPG images or PDF documents

The template repository features four objects from the University of Idaho Library's [Digital Collections](https://www.lib.uidaho.edu/digital). 

For full details of creating your own collection site, visit [CollectionBuilder Documentation](https://collectionbuilder.github.io/cb-docs/)!

