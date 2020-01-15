\$ momo\_
==========

Momo是一个y with as little code as necessary. It's the "Command
Line Interface Creation Kit". It's highly configurable but comes with
sensible defaults out of the box.

It aims to make the process of writing command line tools quick and fun
while also preventing any frustration caused by the inability to
implement an intended CLI API.

Click in three points:

-   Arbitrary nesting of commands
-   Automatic help page generation
-   Supports lazy loading of subcommands at runtime


Installing
----------

Install and update using `pip`_:

.. code-block:: text

    $ pip install --editable .

Click supports Python 3.4 and newer, Python 2.7, and PyPy.

.. _pip: https://pip.pypa.io/en/stable/quickstart/


A Simple Example
----------------

What does it look like? Here is an example of a simple Click program:

.. code-block:: python

    import click

    @click.command()
    @click.option("--count", default=1, help="Number of greetings.")
    @click.option("--name", prompt="Your name",
                  help="The person to greet.")
    def hello(count, name):
        """Simple program that greets NAME for a total of COUNT times."""
        for _ in range(count):
            click.echo("Hello, %s!" % name)

    if __name__ == '__main__':
        hello()

And what it looks like when run:

.. code-block:: text

    $ python hello.py --count=3
    Your name: Click
    Hello, Click!
    Hello, Click!
    Hello, Click!





Links
-----

*   Documentation: https://click.palletsprojects.com/
*   License: `BSD <https://github.com/pallets/click/blob/master/LICENSE.rst>`_
*   Releases: https://pypi.org/project/click/
*   Code: https://github.com/pallets/click
