.. _API:Runner:

Runner
######

This section covers the interface for deciding which workflows to execute, whether to run the in parallel, which
specific parameters to use and how to interpret exit/termination codes of tools, as well as gathering/buffering the
stdout/stderr and partially processing it.
Therefore, the runner API is closely related to :ref:`API:Tool`, both of them belonging to layer 2 (Workflows) of
the :ref:`EDAA:Concept`.

In the case of VUnit, the runner is composed by sibling interfaces written in Python and HDL, due to the limitations in
some older revisions of VHDL to get the termination status.

*TBC*

.. figure:: ../_static/runner_cfg.png
  :alt: Passing runner configuration from Python to HDL
  :width: 500 px
  :align: center

  Strategies to pass the runner configuration from Python to HDL.

* `VUnit/vunit#772 <https://github.com/VUnit/vunit/issues/772>`__

References
==========

* `IEEE-P1076/VHDL-Issues#13: Python API <https://gitlab.com/IEEE-P1076/VHDL-Issues/-/issues/13>`__

* `Test Anything Protocol <https://testanything.org/>`__

  * `python-tap/tappy <https://github.com/python-tap/tappy>`__: a set of tools for working with the TAP in Python.

* `FuseSoc Verification Automation (fsva) <https://github.com/m-kru/fsva>`__ is an HDL testbench runner based on `FuseSoc <https://hdl.github.io/awesome/items/fusesoc/>`__.
  It fetches targets named with certain patterns in ``.core`` files; which can be executed in parallel; stdout/stderr
  are captured and parsed.

* `ttask <https://www.p-code.org/ttask/index.html>`__
