# Introducing Multi Device Switcher

This WordPress plugin allows you to set a separate theme for device (Smart Phone, Tablet PC, Mobile Phone, Game and custom).
This plugin detects if your site is being viewed by UserAgent, and switches to selected theme.
The Custom Switcher can add every device.

## Features

- Set a separate theme for device (Smart Phone, Tablet PC, Mobile Phone, Game), switches to selected theme.
- Add every device by the Custom Switcher.
- Add links 'Mobile' or 'PC' in the theme by the PC Switcher, switch to the default theme.
- Can be using is_multi_device() function that detect of the device.

## How do I use it ?

1. Download and unzip files. Or install multi-device-switcher using the WordPress plugin installer. In that case, skip 2.
2. Upload "multi-device-switcher" to the "/wp-content/plugins/" directory.
3. Activate the plugin through the 'Plugins' menu in WordPress.
4. Upload a separate theme to the "/wp-content/themes/" directory.
5. Go to the "Multi Device Switcher" options page through the 'Appearance' menu in WordPress.
6. Configure settings to your needs. Select Theme by Theme option. Add and fix UserAgent by UserAgent option if necessary.
7. Have fun!

## Screenshot

<img src="screenshot-1.png">
<img src="screenshot-2.png">
<img src="screenshot-3.png">

## How to add the Custom Switcher

1. Go to the "Multi Device Switcher" options page through the 'Appearance' menu in WordPress.
2. Enter the name of the Custom Switcher (20 characters max, alphanumeric) to the 'Add Custom Switcher'. Push the button 'Add'.
3. Configure settings. Select Theme by Theme option. Add UserAgent by UserAgent option.
4. Have fun!

## Setting and Using the PC Switcher

There are three ways how to Using the PC Switcher.

<img src="screenshot-4.png">

### 1. Add a PC Switcher to the footer

1. Go to the "Multi Device Switcher" options page through the 'Appearance' menu in WordPress.
2. Configure settings. Check the checkbox 'Add a PC Switcher to the footer.' by PC Switcher option.
3. Have fun!

### 2. Add a PC Switcher to your sidebars/widget areas

1. Add-on the widget 'PC Switcher', when you activate the plugin "Multi Device Switcher".
2. Go to the "Widgets" options page through the 'Appearance' menu in WordPress.
3. Drag and drop the title bars 'PC Switcher' into the desired area.
4. Have fun!

### 3. For the theme authors and developers, add a PC Switcher to your theme.

1. Add the following code into the PHP files, when you develop your theme.
```
<?php if ( function_exists('multi_device_switcher_add_pc_switcher') ) { multi_device_switcher_add_pc_switcher(); } ?>
```
2. Have fun!

### Using default CSS and customized CSS

1. Go to the "Multi Device Switcher" options page through the 'Appearance' menu in WordPress.
2. Configure settings. Check the checkbox 'Add a default CSS.' by PC Switcher option. If you want to customize CSS, uncheck the checkbox.
3. Have fun!

## UserAgent option Samples

* [Default UserAgent](https://github.com/thingsym/multi-device-switcher/wiki/Default-UserAgent)

## is_multi_device() function

is_multi_device() function is a boolean function, meaning it returns either TRUE or FALSE. Works through the detection of the device by the Multi_Device_Switcher class.

### Usage

```
<?php is_multi_device('smart'); ?>
```

### Examples

```
<?php
if ( function_exists( 'is_multi_device' ) ) {
	if ( is_multi_device('smart') ) {
		/* Display and echo smartphone specific stuff here */
	} elseif ( is_multi_device('tablet') ) {
		/* Display and echo tablet specific stuff here */
	}
}
?>
```

### Parameters

**device name** (required)

(string) The name of the device

* smart
* tablet
* mobile
* game
* the name of the Custom Switcher

### Return Values

(boolean) Return boolean whether a particular device.

## Contributing

### Patches and Bug Fixes 

Small patches and bug reports can be submitted a issue tracker in Github. Forking on Github is another good way. You can send a pull request.

#### Contributors

* hykw [Github](https://github.com/hykw/multi-device-switcher)

### Translations

Translating a plugin takes a lot of time, effort, and patience. I really appreciate the hard work from these contributors.

If you have created or updated your own language pack, you can send [gettext PO and MO files](http://codex.wordpress.org/Translating_WordPress) to author. I can bundle it into Multi Device Switcher.

#### Translator

- Japanese (ja) - <a href="http://global.thingslabo.com/blog/">Thingsym</a>

##### The latest PO and MO files

- [POT file](http://plugins.svn.wordpress.org/multi-device-switcher/trunk/languages/multi-device-switcher.pot)
- [PO files](http://plugins.svn.wordpress.org/multi-device-switcher/trunk/languages/)

##### Send your own language pack

You can send your own language pack to author.

- [multi-device-switcher - GitHub](https://github.com/thingsym/multi-device-switcher)
- [http://global.thingslabo.com/blog/ (en)](http://global.thingslabo.com/blog/)
- [http://blog.thingslabo.com (ja)](http://blog.thingslabo.com)

## Changelog

* Version 1.3.0
	* fixed: fix script, style, html and readme
	* new features: is_multi_device() function
	* fixed: fix translation
	* updated: update default UserAgent
	* fixed: replace WP_PLUGIN_URL with plugins_url()
	* fixed: using Page Hook Suffix
	* merged: pull request [#3](https://github.com/thingsym/multi-device-switcher/pull/3)
* Version 1.2.3
	* fixed: fix redirect uri with query string, using add_query_arg
	* fixed: fix translation
	* fixed: fix readme
* Version 1.2.2
	* improved: improve responsiveness UI
	* fixed: fix html
* Version 1.2.1
	* fixed: delete add_contextual_help
	* fixed: fix readme and html
* Version 1.2.0
	* added: add PC Switcher Widget
	* new features: PC Switcher
	* added: add the settings link to the plugin page
* Version 1.1.2
	* required: at least version 3.4
	* fixed: fix tabs and buttons
* Version 1.1.1
	* fixed: change the order of the UserAgent detection
	* updated: update default UserAgent
	* added: add HTTP/1.1 Vary header
* Version 1.1.0
	* new features: Custom Switcher
* Version 1.0.4
	* fixed: fix the object model PHP5, __construct() to replace Multi_Device_Switcher
	* fixed: wp_get_themes(), and wp_get_theme() to replace get_themes(), get_theme()
* Version 1.0.3
	* updated: update screenshots
	* fixed: fix reset button
* Version 1.0.2
	* added: add file uninstall.php
	* fixed: split admin_enqueue_scripts() into two functions
	* fixed: detects is_admin()
* Version 1.0.1
	* fixed: split multi_device_switcher_init() into two functions
* Version 1.0.0
	* Initial release.

## Upgrade Notice

* 1.1.2
	* Requires at least version 3.4 of the Wordpress

