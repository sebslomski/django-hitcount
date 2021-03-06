Django-HitCount
===============

Basic app that allows you to track the number of hits/views for a particular
object.

*Update 05/15/2015:* I've finally had some time to integrate some changes
and get it up to Django 1.8.x speed.  A pre-1.8 (much older!) version was tagged
`0.2`; I've bumped the version to 1.0dev in case we've introduced any backwards
incompatible changes (which I know we have because we changed the content type
model field types).  Am working on things this month (May 2015) so if you want
to grab a pip version (older) I wouldn't blame you.

Please post issues in the github issue tracker.

For more information you can view comments in the source code or visit:

<http://blog.damontimm.com/django-hitcount-app-count-hits-views/>

What it is not
--------------

This is not meant to be a user tracking app (see: [django-tracking][1]) or a
comprehensive site traffic monitoring tool (see: Google Analytics).

It's meant to serve as a simple hit counter for chosen objects with a couple
useful features (user-agent, session, and IP tracking) and tools to help you
on your way.

Example Project:
----------------

I have added an example project with a simple Blog application so you can
see the hit counting demonstrated.  You can use that to test the functionality and
it should work out of the box with Django 1.8.1 and Python 2.7.x.

You can load some initial fixtures at:

    python manage.py migrate            # will load some data fixtures for you
    python manage.py createsuperuser    # if you want admin access

Settings:
---------

Be sure to add this to your `settings.py`

   SESSION_SAVE_EVERY_REQUEST = True

TODO:
_____

    * Docs (other settings, etc)
    * Tests (not a single test yet!)
    * Internationalization (although this has been started)
    * Port to python 3.x (support django 1.8 versions)
    * Upload to pip repository (need to read about this)

Contribute
----------

I would love to make it better.  Please fork and push.  Some fun additions
might be [1] a nice graphing utility for the admin site, [2] another approach
to capturing a hit (other than jQuery).

Additional Authors and Thanks
__________________

This doesn't include everyone and if I missed someone let me know I will add it.

Thanks goes to:

 * Basil Shubin and his work at <https:/github.com/bashu/django-hitcount-headless>
 * ariddell for putting the `setup.py` package together

[1]:http://code.google.com/p/django-tracking/


