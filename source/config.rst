.. _config:

Config file reference
================================================================================
``config.json`` is a JSON file which contains meta-data about your app. It determines basic settings for your app, such as the name users will see, as well as module config which allows various parts of Forge to be enabled or configured individually.

Modifying ``config.json``
-------------------------

You can edit the file directly using your preferred text editor. It is located in the ``src`` directory. Alternatively, you can edit it through the Toolkit UI by clicking the App config tab in the top right of the app screen:

.. image:: /_static/images/toolkit-app-config.png

Modules
-------

Most of the configuration for apps is available in the form of modules, you can find a list of modules :ref:`in these docs <modules>`. Each module your app uses needs to be included in your ``config.json``, some modules can simply be given the value ``true`` to be enabled, others require their own configuration options. Each modules configuration options can be found within its documentation page.

Field summary
--------------------------------------------------------------------------------
Below is a template of a basic ``config.json`` file with links to a detailed description of each field.

.. parsed-literal::
    {
        ":ref:`name <field-name>`": "My App",
        ":ref:`author <field-author>`": "Forger",
        ":ref:`description <field-description>`": "My First Forge App.",
        ":ref:`version <field-version>`": "1.0",
        ":ref:`platform_version <field-platform-version>`": "v1.3",
        ":ref:`homepage <field-homepage>`": "http://example.com"",
        ":ref:`modules <field-modules>`": {}
        ":ref:`partners <field-partners>`": {},
        ":ref:`config_version <field-config-version>`": "2",
    }


Fields
--------------------------------------------------------------------------------

This section includes more detailed information on the contents of each field, with links to other documentation where appropriate.

.. _field-name:

name
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This will be the name for your app, a short, descriptive name is recommended as in some situations long names may be cut off.

.. _field-author:

author
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This text will be displayed as the author or creator of the app, depending on the platform.

.. _field-description:

description
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*Optional*.

A longer description of what your app does. This description may be displayed to users during and after installation, to let them know what the app does.

.. _field-version:

version
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The version of your app. It must be formatted as up to three dot-separated numbers, e.g. ``1.1`` or ``0.99.9``.

.. _field-platform-version:

platform_version
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

As the Forge platform grows and improves, we may deprecate and remove some functionality. To prevent these updates from breaking your app, use this field to specify the version of the Forge platform you wish to build on top of. See :ref:`release-notes` for more information about platform versions. 

.. _field-homepage:

homepage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*Optional*.

Your website, or location of more information about this app.

.. _field-partners:

partners
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Configuration for 3rd party integration. For more information check :ref:`our partners <partners>`.

.. _field-modules:

modules
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Enable and optionally configure optional modules. For more information check :ref:`individual modules <modules>`.

.. _field-config-version:

config_version
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

An internally used reference to keep track of changes to the Forge config file schema, you shouldn't need to change this property manually.
