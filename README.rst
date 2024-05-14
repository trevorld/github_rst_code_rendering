Tests of rst regressions on Github
-----------------------------------

.. contents::

After **years** of rendering fine it seems that there are recent rendering bugs of
restructuredText files on Github:

* https://github.com/github/markup/issues/1796
* https://github.com/github/markup/issues/1798

Officially `docutils <https://docutils.sourceforge.io/>`_ and most other restructuredText renderers like ``pandoc`` support three source code directives:

* ``code``
* ``code-block``
* ``sourcecode``

Here are some links to their in source code where they support all three of these:

* https://github.com/docutils/docutils/blob/ff0b419256d6b7bfdd4363dd078c2255701de605/docutils/docutils/parsers/rst/languages/en.py#L36
* https://github.com/jgm/pandoc/blob/0c5fd01cb87c179ce8b41dead5d72b7b353d178b/src/Text/Pandoc/Readers/RST.hs#L719

Test of ``code`` directive
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: python

   # Python code
   print(2 + 2)

.. code:: r

   # R code
   print(2 + 2)

Test of ``code-block`` directive
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: python

   # Python code
   print(2 + 2)

.. code-block:: r

   # R code
   print(2 + 2)

Test of ``sourcecode`` directive
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. sourcecode:: python

   # Python code
   print(2 + 2)

.. sourcecode:: r

   # R code
   print(2 + 2)
