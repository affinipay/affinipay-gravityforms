=== Gravity Forms + ChargeIO ===
Tags: form, forms, gravity, gravity form, gravity forms, gravityforms, chargeio, payment, payments, subscribe, subscriptions, recurring billing, paypal, authorize.net, credit cards, online payment
Requires at least: 3.6
Tested up to: 4.1
Beta tag: 0.0.1

Easy and secure credit card payments on your WordPress site with ChargeIO and Gravity Forms!

== Description ==

[ChargeIO](https://chargeio.com) allows you to process credit cards directly on your site, securely and easily, without having to deal with merchant accounts, PCI-compliance, or PayPal. This Gravity Forms add-on integrates ChargeIO with your forms using [ChargeIO.js](https://chargeio.com/developers/paymentint/) to make sure sensitive card information never hits your server.

> This plugin is an add-on for the [Gravity Forms plugin](http://gravityforms.com "visit the Gravity Forms website").
>
> You'll also need a [ChargeIO](https://chargeio.com) account.

Requires WordPress 4.1, PHP 5.3, and Gravity Forms 1.8.1. Works with WordPress Multisite.

**Current Features**

* One-time payments
* International ChargeIO accounts, including those with multiple currencies
* ChargeIO + PayPal option on same form
* Hooks to extend the plugin and add in your own functionality

**Support**

* https://chargeio.com/
* Also, Gravity Forms does not provide support for this plugin.
* If you think you've found a bug or you're not sure if you need to purchase support, feel free to [contact me](dschiera@affinipay.com).

**Current Limitations**

* Cannot have ChargeIO Add-On "activated" at the same time as Authorize.Net, Stripe or PayPal Pro Add-Ons
* For security reasons, credit card field has to be on the last page of a multi-page form
* One ChargeIO form per page

**Reported Conflicts**

* plugin: Shortcodes Ultimate
* plugin: PHP Shortcode Version 1.3
* theme: Themeforest themes that strip shortcodes
* plugin: Root Relative URLs


== Installation ==

This section describes how to install and setup the Gravity Forms ChargeIO Add-On. Be sure to follow *all* of the instructions in order for the Add-On to work properly.

1. Make sure that Gravity Forms is activated
2. Upload the `gravity-forms-chargeio` folder to the `/wp-content/plugins/` directory
3. Activate the plugin through the 'Plugins' menu in WordPress.
4. Add your ChargeIO API keys to the ChargeIO tab on the Settings page (Forms->Settings).
5. Create a form, adding at least one product field along with the new 'Credit Card' field that appears under 'Pricing Fields.' Keep in mind that ChargeIO accepts a minimum charge of $0.50 - this means that the total amount of your form must be at least $0.50.
6. Under Forms->ChargeIO, add a ChargeIO feed for your new form.

== Frequently Asked Questions ==

= Do I need to have my own copy of Gravity Forms for this plugin to work? =
Yes, you need to install the [Gravity Forms Plugin](http://gravityforms.com "visit the Gravity Forms website") for this plugin to work.

= What is the minimum amount my form can accept? =
$0.01

= Does your plugin use ChargeIO.js? =
Yes.

= Do I need to have SSL? =
Yes, according to the ChargeIO Terms of Service regarding PCI-compliance.

= Why am I getting an 'Empty string given for card' error? =
Here are a few possible reasons, listed in the order they are most likely to occur:

1. Your theme (especially if purchased from Themeforest) is stripping the shortcode, preventing the ChargeIO JS from working. Here's what you want to look for in your theme files (the code is in yellow) and disable by placing a '//' without the quotes in front of those lines:
http://kaptinlin.com/support/discussion/7420/gravity-forms-code-of-the-raw-shortcode-discussion-thread/p1

This code may also be in a file called shortcodes.php or ThemeShortcodes.php.

2. Another theme or plugin is modifying the standard Gravity Forms dropdowns and removing the classes, which breaks the ChargeIO JS. You'll want to contact the theme author to learn how to prevent this.

3. You've embedded your Gravity Form directly into the page and missed one of the Gravity Forms instructions Ñ happens to the best of us! Here are the instructions: http://www.gravityhelp.com/documentation/page/Embedding_A_Form

4. Another plugin is preventing the JS from working. Follow the procedure outlined here by Gravity Forms in order to troubleshoot: http://www.gravityhelp.com/documentation/page/Testing_for_a_Theme/Plugin_Conflict with one minor change -- For plugin conflicts, deactivate all plugins except Gravity Forms and Gravity Forms + ChargeIO.

5. JavaScript is not available to browser


== Screenshots ==

1. Settings page
2. Credit Card field
3. ChargeIO feed