Mirror Notes
------------

This is an unofficial mirror of a google code project by Matthew Painter.
I have reproduced it here in hopes of generating interest in extending it to
support the new functionality added in recent API updates.

Project Information
-------------------

SimpleDB/dev provides a local SimpleDB server, so you can develop offline, without even currently having a SimpleDB account.

Now supports Linux, OS X and Windows >= XP.

Currently implemented:

The current 2007-11-07 REST API
* _EVERY Action_ - SimpleDB/dev is functionally complete :o)
* Correct HTTP Error Responses, as per the technical documentation
* A large suite of tests created from the examples provided in the technical documentation

Currently not implemented:
* The SOAP API.
* Authentication - signature value checking.
* Timestamp format and expiration checking.
* HTTPS

To run a SimpleDB/dev server, you'll need python (tested with 2.5, standard with OS X Leopard), and web.py (tested with 0.3.1). You can install web.py easily if you have python's easy install on your path:

    easy_install web.py

If you don't have easy install, you can install it by downloading the bootstrapper ez_install.py, and running it. (Windows users, easy_install.exe is installed in the Scripts directory in your python directory.)

Windows users will have to also install the Python extensions for windows.

So now just download the latest release, and start up the SimpleDB/dev web server:

    python simpledb_dev.py <port number, default 8080>

If the server doesn't start, or you have other problems, it's pretty easy to run the tests and see some examples of request/response:

    python simpledb_dev.py test

Remember, this is a development tool, and not meant for storing or querying large amounts of data - I do not know yet how big you can get before running into issues, but I suspect that with the current storage and querying design it is not that large :o) Now that I have a base, I may start trying to see how I can improve the performance...

Although this conforms to the specifications in the technical documentation, SimpleDB/dev has not been tested with every possible SDB client library, and I am looking forward to people in the oss community trying to find bugs and peculiarities - it is after all, a work in progress!

_So enjoy developing your SimpleDB applications now, not later!_

Matthew Painter

Contributing
------------

1. Fork it.
2. Create a branch (`git checkout -b new_api`)
3. Commit your changes (`git commit -am "Added support for the new API version"`)
4. Push to the branch (`git push origin new_api`)
5. Create an [Issue][1] with a link to your branch

