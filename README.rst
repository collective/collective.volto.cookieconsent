.. This README is meant for consumption by humans and pypi. Pypi can render rst files so please do not use Sphinx features.
   If you want to learn more about writing documentation, please check out: http://docs.plone.org/about/documentation_styleguide.html
   This text does not appear on pypi or github. It is a comment.

====================
Volto Cookie Consent
====================

Add-on for manage Cookie Consent banner on Volto

Features
--------

- Control panel to plone registry to manage cookie consent settings.
- Restapi view that exposes these settings for Volto

Volto endpoint
--------------

Anonymous users can't access registry resources by default with plone.restapi (there is a special permission).

To avoid enabling registry access to everyone, this package exposes a dedicated restapi route with cookie consent config: *@cookieconsent-infos*::

    > curl -i http://localhost:8080/Plone/@cookieconsent-infos -H 'Accept: application/json' --user admin:admin

And the result is something like this::

    {
        "accept_on_click": true,
        "cookie_consent_configuration": {'some':'data'}
    }

Control panel
-------------

You can edit settings directly from Volto because the control has been registered on Plone and available with plone.restapi.


Volto integration
-----------------

To use this product in Volto, your Volto project needs to include a new plugin: **TO-BE-CREATED**


Translations
------------

This product has been translated into

- Italian


Installation
------------

Install collective.volto.cookieconsent by adding it to your buildout::

    [buildout]

    ...

    eggs =
        collective.volto.cookieconsent


and then running ``bin/buildout``


Contribute
----------

- Issue Tracker: https://github.com/collective/collective.volto.cookieconsent/issues
- Source Code: https://github.com/collective/collective.volto.cookieconsent
- Documentation: https://docs.plone.org/foo/bar


Support
-------

If you are having issues, please let us know.
We have a mailing list located at: project@example.com


License
-------

The project is licensed under the GPLv2.
