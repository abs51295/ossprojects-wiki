Systers use a customized version of Mailman 2. We would like to port our features to Mailman 3.  

The features that we want to port are: 

- Essay
- Stats for admins

Note: The [GNU Mailman](http://wiki.list.org/DEV/Google_Summer_of_Code_2015) org also has a project to port the "dynamic sublists" feature to Mailman 3.

The primary implementation language is Python.  [Mailman 3](http://wiki.list.org/DEV/) core has already been ported to Python 3.  The library that will be used in implementing these features is called mailmanclient, which can called from either Python 2 or Python 3.  Most likely both features will be implemented in the Postorius Django application, which provides configuration services to both administrators and users of a Mailman system.  Postorius is in the process of being ported to Python 3 (no estimate for release, but Mailman will be sprinting on this at PyCon 2016 in early June).

Some work has been done on both features in the past, but with Mailman 3 a moving target (in fact, mostly before the public release at PyCon 2015), the Systers code has not yet been released or put into production.  In GSoC 2013, Shanu Salunke (Dardie) did some work on a new comprehensive [Member Interface](http://systers.org/systers-dev/doku.php/gosc2013_memberinterface), which included input of the essay as one panel for new members.  In GSoC 2015, Khushboo Surana (khushboo9293) implemented some [membership statistics](https://github.com/khushboo9293/mailman/tree/Feature-CountUnsubscribers).  Khushboo's code is scheduled to be merged, so future work on "Stats for Admins" should be compatible with it.

For GSoC 2016, we have a Slack channel #mailman3 devoted to Mailman features.  But due to the complexity of the development environment (spanning several versions of two languages and a featureful web framework), you may also get useful advice from Python and Django developers in other channels.
 
## Development Environment
* Difficulty: Intermediate to Advanced
* Language: Python, SQL (SQLAlchemy for Python), Django
* Virtual Environment: [Vagrant VM for Systers Mailman 3](https://github.com/abi-systers/vagrant-systers/tree/master/mm3)
* Production sources: [Systers Mailman 2.12](https://code.launchpad.net/systers)
 
## Mentors
Stephen Turnbull (Mailman core developer, @yaseppochi on Freenode IRC #mailman and Slack)
Ana Cutillas (Systers developer, @acoconut on Slack)
