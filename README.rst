Template for the Read the Docs tutorial
=======================================

This GitHub template includes fictional Python library
with some basic Sphinx docs.

Read the tutorial here:

https://docs.readthedocs.io/en/stable/tutorial/

.. code-block:: Bash

  git clone --depth 1 https://github.com/khiem20tc/read-the-docs.git .
  git fetch origin --force --prune --prune-tags --depth 50 refs/heads/main:refs/remotes/origin/main
  git checkout --force origin/main
  git clean -d -f -f
  cat .readthedocs.yaml
  asdf global python 3.10.12
  python -mvirtualenv $READTHEDOCS_VIRTUALENV_PATH
  python -m pip install --upgrade --no-cache-dir pip setuptools
  python -m pip install --upgrade --no-cache-dir sphinx readthedocs-sphinx-ext
  python -m pip install --exists-action=w --no-cache-dir -r docs/requirements.txt
  cat docs/source/conf.py
  python -m sphinx -T -E -b html -d _build/doctrees -D language=en . $READTHEDOCS_OUTPUT/html

