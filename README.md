ZIDS: Zend Framework Intruder Detection System
==============================================

What is ZIDS?
-------------
In one sentence: ZIDS makes Zend Framework applications more secure!

The longer version: "Never ever trust user input!" - ZIDS helps you to follow this golden rule of programming web applications. ZIDS uses PHP-IDS to analyze user inputs. The impact of a request is an integer value returned by PHP-IDS that indicates the severity of an possible attack. The higher the impact, the more likely the request was an attack!

ZIDS enables you to easily integrate PHP-IDS in your Zend Framework project. It allows you to define any number of impact levels: e.g., 'unlikely', 'likely', 'very likely' and 'attack'.

For each level you may define:

 - an interval that defines how the impact will be categorized, e.g. impact 0-10 will be considered as an 'unlikely' attack whereas an impact between 11 and 30 will be considered as a 'likely' attack.
 - how to deal with an attack, e.g. ignore the attack, log the attack, send an email to the admin, redirect the user to a special side (controller/action), etc. 

Furthermore, ZIDS enables you to aggregate all impacts in your session. This is useful as usually an attacker will start to analyze your website with a series of "small" attacks, i.e. attacks with an impact below 15. If you enable aggregation, four attacks with an impact of 5 will aggregate to an attack with an impact of 20 (5 + 5 + 5 + 5).
Online Manual

Have a look at the [manual here...](http://www.web-punk.com/wp-content/uploads/README_v_1_0_1.html)

Features
--------
 - Easy to install
 - Define any number of impact levels, i.e. define that if the impact returned by PHP-IDS is < 10, the impact level is an "unlikely attack"; if it is < 50, the impact level is a "likely attack", etc.
 - Easy to define how to deal with a possible attack by using out-of-the-box action plugins
  - Ignore: simply ignores an attack
  - Log: log an attack to your Zend_Log instance, e.g. your log file
  - Email: send an email to your webadmin
  - Redirect: redirect the user to a special side 
 - Easily create your own Plugins
 - Define what the Log Plugin should log, e.g. IP-address of the attacker, attack tags, etc.
 - Parameters for all action plugins may be specified globally or for each level
 - Define which module/controller/action should not be analyzed by ZIDS. If you specify only a module, all requests to this module will be ignored. If you specify a module and a controller, all actions in this controller will be ignored. If you specify a module, controller and action, all requests to this action will be ignored.
 - Sometimes it even brews coffee for you! 

Questions?
----------
Got questions? Please contact me using the contact form on [my blog...](http://www.web-punk.com/) 