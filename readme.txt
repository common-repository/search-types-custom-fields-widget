=== Search Widget and WP REST Server for Toolset Types ===
Contributors: Magenta Cuda
Tags: search, custom fields
Requires at least: 3.6
Tested up to: 4.6
Stable tag: 2.2.1
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Search Types custom posts for posts that have user specified values for Types custom fields.

== Description ==

**I have quit active development of this plugin. This means no new features will be added. If you are intending to become a new user of this plugin I recommend you try another product. If you are an existing user don't worry. This plugin is still fully supported. I intend to maintain the existing feature set of this plugin for the foreseeable future. This includes compatibility with future versions of WordPress. However as I no longer personally use this product I will not know about a problem unless a user reports it. You can report a problem using [this plugin's support forum](https://wordpress.org/support/plugin/search-types-custom-fields-widget). But, for the quickest response in addition you should also contact me using [the contact form on my website](http://magentacuda.com/contact-me/).**

This [search widget](http://alttypes.wordpress.com/search-types-custom-fields-widget/) can search [Toolset Types](http://wordpress.org/plugins/types/) custom posts by the value of Toolset Types custom fields, custom taxonomies and parent/child relationships. It is designed to be used with the Toolset Types plugin and makes use of Toolset Types' proprietary database format to generate user friendly field names and field values. The widget uses user friendly substitutions for the actual values in the database, e.g. post title is substituted for post id in parent/child fields. The selected posts can be displayed as a standard WordPress list of posts, a spreadsheet of posts with their custom fields or a gallery of featured images.

Version 1.3 supports a [single-page application mode](https://alttypes.wordpress.com/#spa) where the search results returned by an interactive AJAX request populates a [Backbone.js](http://backbonejs.org/) collection of models which can be rendered in the same page using [Underscore.js](http://underscorejs.org/#template) templates and the [Bootstrap](http://getbootstrap.com/) framework.
You can view a working sample page using this plugin in single-page application mode at [my portfolio website](http://magentacuda.com/demo-of-search-widget-and-wp-rest-server-for-toolset-types/).

[Version 2.0](https://alttypes.wordpress.com/#rest-api) implements an experimental [WP REST API](http://v2.wp-api.org/) server for Toolset Types custom post types and custom fields.

Please visit the [online documentation](http://alttypes.wordpress.com/search-types-custom-fields-widget/) for more details. **This plugin works with Toolset Types 2.2.2 and requires at least PHP 5.4.** [This plugin is not compatible with the WordPress Multilingual Plugin by OnTheGoSystems.](http://wordpress.org/support/topic/incompatibility-between-my-plugin-and-wpml-multilingual)

== Installation ==
1. Upload the folder "search-types-custom-fields-widget" to the "/wp-content/plugins/" directory.
2. Activate the plugin through the "Plugins" menu in WordPress.
3. Activate this widget by dragging it to a sidebar through the "Appearance->Widgets" menu in WordPress.

== Frequently Asked Questions ==
= Does this plugin require that Types plugin to be installed? =
Yes.

= Where is the documentation? =
http://alttypes.wordpress.com/search-types-custom-fields-widget/

= How to use the REST Server? =
To activate the REST server install and activate the [WordPress REST API v2 plugin](https://wordpress.org/plugins/rest-api/). Beware this requires pretty permalinks.
The search widget currently uses an older proprietary AJAX API and does not use the REST server and does not need the WordPress REST API plugin to be installed.
The REST server is experimental and the API is subject to change. 
Please read the [documentation](https://alttypes.wordpress.com/#rest-api).

== Screenshots ==
1. The "Search Widget" interactively loads the "Search Results Pane".

== Changelog ==

= 2.2.1 =
* added automatic generation of user templates
* fix HTML validation errors

= 2.2 =
* added support for a JavaScript/Backbone client
* enhanced the REST search by taxonomy, child-of and parent-of to accept both ids and titles

= 2.1 =
* added support for select, radio and checkbox Toolset Types custom fields to REST API
* replaced term id with term name or slug for taxonomy fields in REST API
* fix bug where search widget tries to use previously deleted custom post type

= 2.0 =
* implements a [WP REST API server](https://alttypes.wordpress.com/#rest-api).
* much better support for user templates.
* bug fixes and css tweaks.

= 1.3.1 =
* fix a security hole
* support for preloading the search results pane
* improved carousel
* tweaks to the user interface

= 1.3 =
* supports dynamically loading via AJAX the search results into the current page instead of loading a new page, i.e. supports the single-page application paradigm.
* replace ugly full viewport carousel view with an inline embedded carousel view
* add mobile swipe to carousel view
* bug fixes and css enhancements

= 1.2.0.1 =
* fix broken widget admin interface

= 1.2 =
* Added option to show the search results using a responsive Twitter Bootstrap stylesheet.

= 1.1.1.1 =
* update the .pot file

= 1.1.1 =
* Make the Backbone.js mode gallery responsive.

= 1.1 =
* Add facility for invoking a function after a Backbone.js template has been rendered - usful for attaching event listeners on the rendered elements.
* Added the popup feature of the classic mode gallery to the new backbone mode gallery.

= 1.0 =
* The front-end re-written as a single-page web application using a Backbone.js Model-View-Presenter - you can select either classic mode or backbone mode.
* You can specify your own Underscore.js template to customize the displayed results - see stcfw-search-results-template.php.

= 0.5.1 =
* The gallery of featured thumbnail images supports mouse-over popups implemented by a Backbone.js view using a optionally user supplied Underscore.js template.
= 0.5 =
* the search results can optionally be displayed as a gallery of featured images of the selected posts. The featured images have a clickable link back to their posts.
= 0.4.9 =
* added a filter &quot;stcfw_display_value&quot; for field values; the filter allows you to translate the raw field value before it is displayed
= 0.4.8 =
* Added localization - use _e() and __(), provide .pot file.
* Code rewritten to improve software quality.
* Tested up to WordPress 4.3 Release Candidate (4.3-RC2-33585).
= 0.4.7.1.1 =
* fix javascript bug
= 0.4.7.1 =
* fix bug where javascript handlers were not always installed when widget was dynamically inserted or replaced in administrator's widget page
* use auto generated excerpt if no user supplied excerpt
* replace taxonomy slug with name
* use simplified labels for checkbox values in search result table
* tested up to WordPress 4.3 Release Candidate (4.3-RC1-33519)
= 0.4.7 =
* code rewritten to fix bugs, enhance security and improve software quality
* added option to use simplified labels for select, checkboxes and radio button values
* replaced field slug with field title
* changed some css to prettify things
= 0.4.6.1.3 =
* another fix for the problem with custom field of type 'Checkboxes' with version 1.6.3 of Types
= 0.4.6.1.2 =
* fix problem with custom field of type 'Checkboxes' with version 1.6.3 of Types
= 0.4.6.1.1 =
* no new features; some small enhancements, bug fixes and code maintenance
* taxonomy items are no longer required to come before other items in the sort order
* it is now possible to choose to display post content in the table of posts which will actually display the post excerpt
* administrator's interface is now stylable using a .css file
= 0.4.6.1 =
* fixed search by tags by input box bug
* added style sheet for search widget
= 0.4.6 =
* added support for sortable tables for search results.
= 0.4.5.3 =
* added search by post author
* added support for post type specific css files
* fix pagination bug
* fix several other bugs
= 0.4.5 =
* optionally display seach results in a table format
* optionally set query type to is_search so only excerpts are displayed for applicable themes
* supports drag and drop to change order of fields
= 0.4.4 =
* added range search for numeric and date custom fields
= 0.4.3 =
* separated child of/parent of categories by post type
* made items shown per custom field user settable
* fixed to handle corrupt obsolete data without crashing
* fixed incorrect counts due to double counting and counting blank and null values
* tweaked the display of checkboxes, select and radio custom fields
= 0.4.2 =
* add support for selecting and/or on search conditions
= 0.4.1.1 =
* Initial release.

== Upgrade Notice ==
= 2.2.1 =
* added automatic generation of user templates
* fix HTML validation errors
= 2.2 =
* added support for a JavaScript/Backbone client
* enhanced the REST search by taxonomy, child-of and parent-of to accept both ids and titles
= 2.1 =
* added support for select, radio and checkbox Toolset Types custom fields to REST API
* replaced term id with term name or slug for taxonomy fields in REST API
* fix bug where search widget tries to use previously deleted custom post type
= 2.0 =
* implements a [WP REST API server](https://alttypes.wordpress.com/#rest-api).
* much better support for user templates.
* bug fixes and css tweaks.
= 1.3.1 =
* fix a security hole
* support for preloading the search results pane
* improved carousel
* tweaks to the user interface
= 1.3 =
* supports dynamically loading via AJAX the search results into the current page instead of loading a new page, i.e. supports the single-page application paradigm.
* replace ugly full viewport carousel view with an inline embedded carousel view
* add mobile swipe to carousel view
* bug fixes and css enhancements
= 1.2.0.1 =
* fix broken widget admin interface
= 1.2 =
* Added option to show the search results using a responsive Twitter Bootstrap stylesheet.
= 1.1.1.1 =
* update the .pot file
= 1.1.1 =
* Make the Backbone.js mode gallery responsive.
= 1.1 =
* Add facility for invoking a function after a Backbone.js template has been rendered - usful for attaching event listeners on the rendered elements.
* Added the popup feature of the classic mode gallery to the new backbone mode gallery.
= 1.0 =
* The front-end re-written as a single-page web application using a Backbone.js Model-View-Presenter - you can select either classic mode or backbone mode.
* You can specify your own Underscore.js template to customize the displayed results - see stcfw-search-results-template.php.
= 0.5.1 =
* The gallery of featured thumbnail images supports mouse-over popups implemented by a Backbone.js view using a optionally user supplied Underscore.js template.
= 0.5 =
* the search results can optionally be displayed as a gallery of featured images of the selected posts. The featured images have a clickable link back to their posts.
= 0.4.9 =
* added a filter &quot;stcfw_display_value&quot; for field values; the filter allows you to translate the raw field value before it is displayed
= 0.4.8 =
* Added localization - use _e() and __(), provide .pot file.
* Code rewritten to improve software quality.
* Tested up to WordPress 4.3 Release Candidate (4.3-RC2-33585).
= 0.4.7.1.1 =
* fix javascript bug
= 0.4.7.1 =
* fix bug where javascript handlers were not always installed when widget was dynamically inserted or replaced in administrator's widget page
* use auto generated excerpt if no user supplied excerpt
* replace taxonomy slug with name
* use simplified labels for checkbox values in search result table
* tested up to WordPress 4.3 Release Candidate (4.3-RC1-33519)
= 0.4.7 =
* code rewritten to fix bugs, enhance security and improve software quality
* added option to use simplified labels for select, checkboxes and radio button values
* replaced field slug with field title
* changed some css to prettify things
= 0.4.6.1.3 =
* another fix for the problem with custom field of type 'Checkboxes' with version 1.6.3 of Types
= 0.4.6.1.2 =
* fix problem with custom field of type 'Checkboxes' with version 1.6.3 of Types
= 0.4.6.1.1 =
* no new features; some small enhancements, bug fixes and code maintenance
* taxonomy items are no longer required to be before other items in the sort order
* it is now possible to choose to display post content in the table of posts which will actually display the post excerpt
* administrator's interface is now stylable using a .css file
= 0.4.6.1 =
* fixed search by tags by input box bug
* added style sheet for search widget
= 0.4.6 =
* added support for sortable tables for search results.
= 0.4.5.3 =
* added search by post author
* added support for post type specific css files
* fix pagination bug
* fix several other bugs
= 0.4.5 =
* optionally display seach results in a table format
* optionally set query type to is_search so only excerpts are displayed for applicable themes
* supports drag and drop to change order of fields
= 0.4.4 =
* added range search for numeric and date custom fields
= 0.4.3 =
* some enhancements and bug fixes
= 0.4.2 =
add support for selecting and/or on search conditions
= 0.4.1.1 =
* Initial release.

