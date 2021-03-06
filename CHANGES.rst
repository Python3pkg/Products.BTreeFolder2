Changelog
=========

4.0 (unreleased)
----------------

- added tox configuration

- Python 3 compatibility

- Update to require and be compatible with Zope 4.

3.0 (2016-07-18)
----------------

- Update Dependencies (no ZODB, but BTrees)

2.14.0 (2015-06-18)
-------------------

- Require ExtensionClass >= 4.1a1 (Compatible w/ Zope 4).

2.13.5 (2015-06-18)
-------------------

- Added case for clean-up routine where the meta type index contains
  keys that are not in the tree.

2.13.4 (2011-12-12)
-------------------

- Provide security declaration for `BTreeFolder2Base.hasObject` method.

- Add some tests for correct `getattr` behavior.

- Minor `__getattr__` and `_getOb` optimizations.

2.13.3 (2011-03-15)
-------------------

- `keys`, `values` and `items` methods are now exactly the same as
  `objectIds`, `objectValues` and `objectItems`. They did the same before
  already but duplicated the code.

2.13.2 (2011-03-08)
-------------------

- `objectValues` and `objectItems` no longer do a special handling when no
  special `spec` is requested as `objectIds` already does the correct
  handling.

2.13.1 (2010-08-04)
-------------------

- Make sure that methods returning objects return them Acquisition wrapped.

- Be more careful in calling our own keys, values and items methods, as
  sub-classes might have overridden some of them.

2.13.0 (2010-07-11)
-------------------

- Changed the `objectIds`, `objectItems` and `objectValues` methods to use the
  internal OOBTree methods directly if no `spec` argument is passed.

- Change implementation of `keys`, `items` and `values` method to access the
  `self._tree` OOBTree methods directly. This avoids lookups in the meta_types
  structures.

- Implement the full dictionary protocol including `__getitem__`,
  `__delitem__`, `__setitem__`, `__nonzero__`, `__iter__` and `__contains__`.

- Released as separate package.
