About
=====

This here is a library for using the `Urban Airship
<http://urbanairship.com/>`_ web service API for iPhone push notifications.

Requirements
============

Tested on Python 2.5 and 2.6 -- it'll probably work on earlier versions. If
you're using Python 2.5 or earlier, you'll need to install ``simplejson``.

Functionality
=============

For this first release it only does two things: device token registration and
basic push. More will be added soon.

Usage
=====

.. sourcecode:: pycon

    
    >>> import urbanairship
    >>> airship = urbanairship.Airship(application_key, master_secret)
    >>> airship.register('valid_token', alias='adam')
    >>> airship.push({'aps': {'alert': 'Hello'}}, aliases=['adam'],
    ...     device_tokens=['some_other_token'])


Questions
=========

The best place to ask questions is our developers mailing list:
http://groups.google.com/group/urbanairship-dev

History
=======

 * 0.1 Initial release