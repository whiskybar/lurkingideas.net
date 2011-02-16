My blog
=======

`lurkingideas.net <http://lurkingideas.net>`_ is a blog site powered by `reStructuredText <http://docutils.sourceforge.net/rst.html>`_ written
in `Django <http://www.djangoproject.com>`_.


Features
--------

* Use reST both for the article preview and the article content.
* Caching the rendered HTML content.
* Draft (unpublished yet) articles.
* Tagging articles.
* RSS feeds for the main page and the articles by tag.


Installation
------------

Ideally, you should fork the project or use it as a template for your blog.
To try it out, clone it locally and modify::

    git clone git://github.com/whiskybar/lurkingideas.net.git

Then, install the blog dependencies::

    cd lurkingideas.net
    pip install -r requirements.txt

Set up your ``virtualenv`` or update your configuration::

    add2virtualenv `pwd` #or plainly, export PYTHONPATH=`pwd`
    export DJANGO_SETTINGS_MODULE=lurkingideas.settings

Initialize the database and you should be ready to launch the development
version of it::

    django-admin.py syncdb
    echo 'DEBUG = True' >>lurkingideas/local_settings.py
    echo 'TEMPLATE_DEBUG = DEBUG' >>lurkingideas/local_settings.py
    django-admin.py runserver


Configuration
-------------

This blog uses SQLite and stores the database into the project directory
for simplicity.

You would want to customize your templates and their graphics design in
particular. I used `FreeCSSTemplates <http://www.freecsstemplates.org/>`_ to
find one.
