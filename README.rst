Introduction
------------


Requirements
------------
Before running the buildout make sure you have the header files of liblxml2 and libxslt::

    sudo aptitude install libxslt1-dev libxml2-dev


Buildout
--------
Clone this repository::

    git clone

You are now ready to run buildout::

    cd wsgi-plone/
    python2.6 bootstrap.py
    ./bin/buildout -v

Starting
--------
To start Plone simply run::

    ./bin/supervisord

To check if everything is working::

    ./bin/supervisorctl status

Should show something like::

    gunicorn                         RUNNING    pid 17955, uptime 0:00:09
    zeo                              RUNNING    pid 17956, uptime 0:00:09

If you want to stop it, run::

     ./bin/supervisorctl shutdown

Now visit http://127.0.0.1:8000 to create a new Plone site.

    .. warning::

    Sunburst conflicts with plone.classic theme. For sunburst to work deactivate Plone Classic theme from Site Setup -> Add-ons
