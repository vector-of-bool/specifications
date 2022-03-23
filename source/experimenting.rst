This page is for experimenting on rST features in GitHub preview
################################################################

..
    This is a comment and should not render

``.. option``
=============

.. option:: test-option

    This is the option body

    .. note::

        This is an embedded note

    this is outside of the note

.. _exper.highlight:

``.. highlight``
================

.. highlight:: python

This code below should be highlighted as Python::

    import os

    def main() -> int:
        ...

.. highlight:: c

This code should now be C::

    #include <stdlib.h>

    #define OUCH

    void foo() {
        return 12;
    }

``:ref: references``
====================

:ref:`This text should link to the "highlight" section <exper.highlight>`

This should be a link to ``.. highlight``: :ref:`exper.highlight`

This should be a link to TestSection1: TestSection1_

This should be a link to TestSection1: `I am a link <TestSection1_>`_

This should be a link to Test Section 2: `Test Section 2`_

This should be a link to Test Section 2: `I am another link <Test Section 2_>`_

This should be a link to the option in ``.. option``: :option:`test-option`

This should be a link to the option in ``.. option``: :option:`I am a link <test-option>`


TestSection1
============

This is just a normal text section


Test Section 2
==============

This is just another normal text section


CSV Table
=========

This is a CSV table:

.. csv-table:: I am a table

    Heading 1, Heading 2
    row 1 col 1, row 1 col 2
    row 2 col 1, row 2 col 2


List Table
==========

This is a list table:

.. list-table:: I am a table

    - - Heading 1
      - Heading 2
    - - Row 1 col 1
      - Row 1 col 2
    - - Row 2 col 1
      - Row 2 col 2


JS function
===========

.. js:function:: func(foo, bar, baz)

    :param foo: I am the ``foo`` param
    :param bar: I am the ``bar`` param
    :param baz: I am the ``baz`` param
    :returns: I am the return text

    I am the documentation block.

    .. note::

        I am an embedded note under the function

I am text outside of the function block.

This should be a link to the function: :js:func:`I am a link <func>`

Doc links
=========

This should be a link to the CRUD page: :doc:`../crud/crud`

This should be a link to the CRUD page: :doc:`I am a link <../crud/crud>`

This should be a link to a section in the server-write-commands page: :ref:`I am a link <insert>`

This should be a link to another section: :ref:`algorithm for filtering by staleness`


External Links
==============

This should be a simple link: `I am a link <https://example.com>`_

This should be a labelled link: `I am a named link <link-name1_>`_

This should be an anonymous link: `I am an anon link <https://wikipedia.org>`__

This should be a different anonymous link: `I am an anon link <https://google.com>`__

This should be an anon inline link with a split target: `Link text`__

.. __: https://github.com

This should be an anon inline link with a split target: `Link text 2`__

__ https://github.com/

.. _link-name1: https://wikipedia.org


Inline roles
============

.. role:: python-code(code)
    :language: python

Here are some inline roles:

- Literal: :literal:`some literal text`
- Code: :code:`foo(bar, baz=24)`
- Python code: :python-code:`import sys; sys.exit(42); foo(bar='baz')`
- Italic: :emphasis:`Emphasized`
- Bold: :strong:`Strong text`
- Superscript: E = mc\ :superscript:`2`
- Subscript: H\ :subscript:`2`\ O
- Math: :math:`E = mc^2`
