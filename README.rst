pytest-testdox
==============

.. image:: https://travis-ci.org/renanivo/pytest-testdox.svg?branch=master
    :target: https://travis-ci.org/renanivo/pytest-testdox

.. image:: https://codecov.io/gh/renanivo/pytest-testdox/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/renanivo/pytest-testdox

A `TestDox format`_ reporter for pytest

.. _TestDox format: https://en.wikipedia.org/wiki/TestDox

.. image:: http://i.imgur.com/rJRL4x9.png

Install
-------

::

    pip install pytest-testdox


Usage
-----

Add the parameter `--testdox` when running `pytest`. Ex:

::

    pytest --testdox your-tests/

Tip: If you don't want to type ``--testdox`` every time you run ``pytest``, add it
to `addopts <https://docs.pytest.org/en/latest/customize.html#confval-addopts>`_
in your `ini file <https://docs.pytest.org/en/latest/customize.html#initialization-determining-rootdir-and-inifile>`_. Ex:

.. code-block:: ini

    # content of pytest.ini
    # (or tox.ini or setup.cfg)
    [pytest]
    addopts = --testdox


Configuration file options
--------------------------

testdox\_format
~~~~~~~~~~~~~~~

Specifies TestDox report format, ``plaintext`` or ``utf8`` (default:
``utf8``). Ex:

.. code:: ini

    # content of pytest.ini
    # (or tox.ini or setup.cfg)
    [pytest]
    testdox_format = plaintext

::

    $ pytest test_demo.py
    ============================= test session starts ==============================
    platform darwin -- Python 3.5.0, pytest-3.0.7, py-1.4.33, pluggy-0.4.0
    rootdir: /private/tmp/demo, inifile: pytest.ini
    plugins: testdox-dev
    collected 2 items

    test_demo.py
    Pytest Testdox
     [x] prints a BDD style output to your tests
     [x] lets you focus on the behavior
