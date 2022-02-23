# Change Log

### v3.3.1
Febryary 23, 2022

* Fix compatibility with Meteor 2.6

### v3.3.0
July 19, 2021

* Rename to montiapm:debug
* Add MontiDebug export as alias to KadiraDebug
* Replace `meteorhacks:kadira` with `montiapm:agent`
* Fix compatibility with Meteor 1.11 and newer

### v3.2.2
23-March-2016

* Only add Blaze related stuff (only event tracking), if only blaze exists in the project.

### v3.2.1
15-March-2016

* Add proper FlowRouter support. Earlier it was not depended weakly. Now we've added support for flow-router-ssr as well.

### v3.2.0
11-March-2016

* Save traces and events inside a Mongo capped collection. This helps us to work with multi-host apps and remote debugging.

### v3.1.1
11-March-2016

* Track routes for kadira:flow-router. Earlier, it was meteorhacks:flow-router.

### v3.1.0
04-March-2016

* Remove blaze activity tracking.
* Correctly use performance.now()

### v3.0.1
* Remove cosmos:browserify since we are not using any npm modules in client.

### v3.0.0
* Now Kadira Debug works in production as well.

#### v2.2.4
* Add check package and now it's possible to use this package with Meteor 1.2

#### v2.2.3
* Fix typo `elasedTime`

#### v2.2.2
* Sending unique keys to determine the version of client and server side of the app. Those keys are used to detect HCR on Kadira Debug UI.

#### v2.2.1
* Update kadira to 2.23.x. It has Meteor 1.2 support

#### v2.2.0
* Tracking traces and time related information to build the DDP timeline

#### v2.1.0
* Track eventloop blockness as a percentage. It's not very clear to reason

#### v2.0.1
* Add old version removal notice. We need to do this because our older version is a different package.

#### v2.0.0
* Add system metrics support
* Move project to kadira

#### v1.3.3
* Set view context to autruns runs inside Templates. Fixes [#7](https://github.com/meteorhacks/kadira-debug/issues/6)

#### v1.3.2

* Allow to use apps on Firefox. Fixes [#6](https://github.com/meteorhacks/kadira-debug/issues/6).

#### v1.3.1

* Check userAgent for string in the method `kadira.debug.getBrowserName`

#### v1.3.0
* Use the actual browser name as the browseId. For this we parse, the userAgent. But, we don't parse it on the client. Instead, we do it on the server. By doing that, we don't need to send some additional code to the client. (ua-parser code)

#### v1.2.0
* Track live updates in a very efficient way. For now, we only track the count and collection only. We don't track fields yet.
* Fixed an issue with our use of time to send data.

#### v1.1.0
* Add a set of testing covering almost all of the code base

#### v1.0.1

* Fix a potential rendering issue. See [#1](https://github.com/meteorhacks/kadira-debug/issues/1)
* Template event's event get tracked before the activity. That makes the

#### v1.0.0

* Initial release without any critical issues or bugs.
