.. image:: https://travis-ci.org/felipeam86/otwrapy.svg?branch=master
    :target: https://travis-ci.org/felipeam86/otwrapy

.. currentmodule:: otwrapy

:code:`otwrapy` is a collection of tools that simplify the task of wrapping
external codes in a Python environment as well as parallelizing it. It is built
on top of `OpenTURNS <http://www.openturns.org>`_, with its users as the target
audience. Documentation is available
`here <http://felipeam86.github.io/otwrapy/>`_. The module provides :

- A :code:`Parallelizer` class that converts any
  `ot.NumericalMathFunction <http://doc.openturns.org/openturns-latest/sphinx/user_manual/_generated/openturns.NumericalMathFunction.html#openturns.NumericalMathFunction>`_
  into  a parallel wrapper using either
  `multiprocessing <https://docs.python.org/2/library/multiprocessing.html>`_,
  `ipyparallel <http://ipyparallel.readthedocs.io/en/latest/>`_,
  `joblib <https://pythonhosted.org/joblib/>`_ or
  `pathos <https://pypi.python.org/pypi/pathos>`_.
- A set of usefull tools that simply recurrent tasks when writing code
  wrappers:

  - :code:`TempWorkDir`: Context manager that gracefully creates a temporary
    working directory. It handles errors and has the option to cleanup upon
    exit.
  - :code:`Debug`: Decorator that protects the decorated function into a
    try/except structure so that errors are logged. It is specially useful
    when you launch your code in a non interactive environment.
  - :code:`load_array` and :code:`dump_array`: Used for efficiently create
    and load backups with the option to compress with gzip.
  - :code:`safemakedirs`: Create a directory without raising an exception if
    it exits.
  - :code:`create_logger`: Return a logger with a FileHandler at a given
    logging level.

:code:`otwrapy` comes from the experience of wrapping a lot of
different external codes at `Phimeca engineering
<http://www.phimeca.com>`_. We are a company specialized in
uncertainty treatment and we assist our clients introducing the
probabilistic dimension in their so far deterministic studies.



.. warning::
    While fully usable, otwrapy is still pre-1.0 software and has **no**
    backwards compatibility guarantees until the 1.0 release occurs! Please
    make sure to be careful **anytime you upgrade**!


