=== Simple Crumbs Redux ===
Contributors: Doug Sparling
Tags: breadcrumbs, navigation
Requires at least: 2.7
Tested up to: 3.6
Stable tag: 1.0.0


Summary: Generates navigation bread crumbs in WordPress. Requires permalinks.

== Description ==

Simple Crumbs Redux is a resurrection of the Simple Crumbs plugin by Can Koluman (http://wordpress.org/plugins/simple-crumbs/) 0.2.5 codebase. Version 1.0.0 of Simple Crumbs Redux fixes a fatal error generated when using PHP 5.4 and greater (and a deprecation warning with PHP 5.3). I'm keeping the original short code (though you can also use [simple_crumbs_redux]) so this plugin will work as a drop in replacement for Simple Crumbs.

Simple Crumbs Redux - Generates a breadcrumb trail for pages and blog entries. Requires use of permalinks and PHP >= 4.1.0. Tested up to WordPress 3.6 and PHP 5.5.

**Notes:** link/crumb information from $query_string, page/post information from $post, using permalink info for making links, using permalink structure for bootstrapping unrolled recursions (deepest to topmost).
Author URI: http://www.dougsparling.org



**Usage Examples:**
---------------------------------- 
*  Usage: `<?php echo do_shortcode('[simple_crumbs root="Home" /]') ?>`
*  Usage: `[simple_crumbs root="Some Root" /]`
*  Usage: `[simple_crumbs /]`


**Sample Output:** (with Home as 'root')
----------------------------------
1. Home > Section > Subsection
1. Home > Blog > 2013 > 08 > 23 > Blog Title
1. Home > Search Results
1. Home > Tag > Tag Name


== Changelog ==


Version: 1.0.0
* Fixed 'PHP Fatal error: Call-time pass-by-reference has been removed' with PHP 5.4 and greater.
* Converted plugin from functional style to Object Oriented.
* Repaced sc_unpack_query_string function with WordPress core function wp_parse_args().


Released under GNU v2 June 1991


== Installation ==

A. Configuration Options
----------------------------------
1. Document Root Crumb name passed to function.
1. Following css class may be defined externally: navCrumb.lnk if needed.
1. Separator may be chosen.


B. Installation
----------------------------------
1. Copy to plugins (`/wp-content/plugins/`) folder
1. Usage:
* from php: `<?php echo do_shortcode('[simple_crumbs root="Home" /]') ?>`
* from html with document root: `[simple_crumbs root="Some Root" /]`
* from html without document root: `[simple_crumbs /]`
