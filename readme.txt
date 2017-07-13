=== Plugin Name ===
Contributors: WebsiteBakery
Donate link: http://freshlybakedwebsites.net/say-thanks-with-a-beer/
Tags: events, calendar, housekeeping, clean up, database, tidy
Requires at least: 3.5.1
Tested up to: 3.5.1
Stable tag: 1.2.2
License: GPL3 or later
License URI: http://www.gnu.org/licenses/gpl.html

Love your database. Keep expired events under control.

== Description ==

Developed to work with _The Events Calendar 3.0,_ this plugin allows for expired events to be automatically vacuumed up rather than leaving them to clutter up your database.

* Configurable: clean up events almost as soon as they have expired or enforce a buffer period of 1 week upto 6 months
* Recurring events are intelligently curtailed (the expired instances will be removed, other events remain untouched)

By default, the plugin schedules clean-up tasks to run once a day and limits itself to handling a maximum of 100 events at any one time. This can be adjusted programmatically for special cases.

Can't get it to work? Check out the FAQs in the first instance and if that doesn't work feel free to post on the
[plugin support forum](http://wordpress.org/support/plugin/the-events-calendar-housekeeper).

= Author =
This plugin was written by [Barry Hughes](http://codingkills.me "WordPress and PHP Developer based in BC, Canada") _(it is not an official plugin by Modern Tribe, so don't go pestering them for support)._ If this helps you out then
[buy the plugin author a beer!](http://freshlybakedwebsites.net/say-thanks-with-a-beer/) More than anything, it will make you feel good about yourself.

== Installation ==

Like any other plugin you simply upload the plugin directory to the wp-content/plugins directory. You can also upload and install it through the WordPress plugins admin page.

*Remember that a prerequisite is the existence of The Events Calendar 2.0.9* (though the latest version targets The Events Calendar 3.0).

Once installed and activated a new "Housekeeping" tab will appear on the Events > Settings page. You must enable garbage collection via this tab or it will not do anything.

== Frequently Asked Questions ==

= How do I enable garbage collection? =

Visit _Events > Settings > Housekeeping_ ... if you can't see this tab then make sure you have activated the plugin, first of all! Remember also that the current version of
_Housekeeper_ is built to work with The Events Calendar 3.0. If for example you are using a much older version then it may not work.

= I have enabled garbage collection but nothing happens! =

Assuming the expiry criteria is being met then this could be a problem where local loopbacks are not allowed within your hosting environment. _Housekeeper_ relies on something called
"Scheduled Tasks" so that it can work its magic in the background, as it were. However not all hosting environments are conducive to this. If you think that might be the problem then
check in with your hosting provider and/or search for "alternative cron solutions".

= How are recurring events handled? =

Any instances of recurring events meeting the _Expiry Criteria_ are deleted - those instances not meeting the criteria are preserved. This seemed like the most logical way to approach recurring events but any other ideas are welcome.

= What if the wrong events are deleted? =

That's completely possible for a variety of reasons. First of all, ensure your server and WordPress date/time settings are correct. Second, but more importantly, back-up before you use it and then keep on backing-up, frequently and often.
You _should_ be doing this anyway - and remember! - a back-up is useless unless you know how to restore it.

= Are they trashed or deleted out-right? =
They are deleted out right. So don't confuse this with the "Trash" function WordPress provides for pages, posts and many custom post types. With this plugin, any events deemed to have expired will effectively be wiped out forever.

= Does an event expire after it has started or after it has ended? =

In the eyes of this plugin an event has expired after it has started and this is flagged up in the settings tab. That may not always be ideal - and for those cases you
can adjust the expiry criteria appropriately or just deactivate this plugin.

= I found a bug =

Please post details on the forum. Better yet, post a fix and add appropriate details. This is free and open source software and comes with no guarantees, so bear that
in mind first of all.

= I need help! =

Feel free to post on the support forum, but remember that support is not guaranteed (nor is the plugin) ... after all, it's free.

== Screenshots ==

1. The Housekeeping tab in Events > Settings

== Changelog ==

= 1.2.2 =
* Fix: expiry criteria of one year now respected (props [Andy Fragen](http://thefragens.com/blog/))

= 1.2.1 =
* Improvement in preflight checks

= 1.2.0 =
* Updated for The Events Calendar 3.0
* Definition of expiry now based on event start date
* Fixed issue where default table prefixes were assumed
* Improved handling of recurring events

= 1.0.3 =
* Recurring event logic added.
* General release.

== Upgrade Notice ==

No major updates yet!