.. Copyright © 2012 Martin Ueding <dev@martin-ueding.de>

################
octave-unitprint
################

::

    unitprint(data)

Prints the associated value and error with the given unit.

It assumes that there is a ``data.val`` in the struct ``data`` that is given as
a parameter. If there is a ``data.unit``, that will be displayed.  If there is
a ``data.err`` key, it will be displayed with the relative error.

If ``data.lit`` it given, the deviation from the literature value is calculated
and displayed also. If ``data.err`` is present, it will be checked, whether the
measurement is close enough to the literature value. If so, it will display a
checkmark, a cross otherwise.

It will print data like this::

    name = value ± error (relative error) unit [deviation checkmark]
