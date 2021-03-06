
myiapws
=======

Myiapws is a python library for the calculation of thermophysical properties of water.  It is an implementation of certain formulations from the [International Association for the Properties of Water and Steam](http://www.iapws.org/) (IAPWS).

The primary use of the library is as an educational tool.  The publications describing the formulations map directly to the code.  The interfaces are simple, fully pythonic and [numpy](http://www.numpy.org/)-capable.

Developers interested in an advanced thermodynamics package covering over 100 fluids should check out [CoolProp](http://www.coolprop.org/).


Installation
------------

Install into python3 by executing (as root)

~~~
# pip3 install git+https://github.com/tomduck/myiapws.git
~~~

Alternatively, download the source and run (as root) `setup.py install`.

The library should be tested (as a normal user) by executing

~~~
$ cd test
$ ./test.py
~~~

The unit tests are based on "computer program verification" values provided by IAPWS.


Modules
-------

The available modules are as follows:

  * `myiapws.iapws1992`: Thermodynamic properties on the coexistence curve of liquid water and vapor.  ([REF](http://www.iapws.org/relguide/supsat.pdf))

  * `myiapws.iapws1995`: Thermodynamic properties of ordinary water substance (liquid and gas).  The fundamental equation is in Helmholtz representation, and so all properties are functions of temperature and density. ([REF](http://iapws.org/relguide/IAPWS95-2014.pdf))

  * `myiapws.iapws2006`: Thermodynamic properties of ice Ih.  The fundamental equation is in Gibbs representation, and so all properties are functions of temperature and pressure. ([REF](http://iapws.org/relguide/Ice-Rev2009.pdf))

  * `myiapws.iapws2011`: Melting and sublimation pressures of liquid water and ice as a function of temperature. ([REF](http://www.iapws.org/relguide/MeltSub2011.pdf))

The modules are internally documented.  Execute `help(<module-name>)` at the python prompt to get full descriptions of each API.


Examples
--------

It is frequently not trivial to draw thermodynamic diagrams given the fundamental equations and their derivatives alone.  The 1995 formulation, for example, provides thermodynamic functions dependent upon density and temperature.  If one wants to, say, plot heat capacity against pressure and temperature instead then some numerical work needs to be done.

Code for the following plots may be found in the `examples/` directory:

![Heat capacity of liquid water at normal pressure.](https://rawgit.com/tomduck/myiapws/master/images/cp.svg)

![Isobaric thermal expansion coefficient of liquid water at normal pressure.](https://rawgit.com/tomduck/myiapws/master/images/alpha.svg)

![Specific volume of liquid water and ice at normal pressure.](https://rawgit.com/tomduck/myiapws/master/images/v.svg)

![Enthalpies for saturated states.](https://rawgit.com/tomduck/myiapws/master/images/hsat.svg)

![Enthalpies of transformation.](https://rawgit.com/tomduck/myiapws/master/images/l.svg)

![Pressure-volume isotherms.](https://rawgit.com/tomduck/myiapws/master/images/pv.svg)

![Temperature-entropy isobars.](https://rawgit.com/tomduck/myiapws/master/images/Ts.svg)

![Mollier diagram.](https://rawgit.com/tomduck/myiapws/master/images/mollier.svg)

![Coexistence curves.](https://rawgit.com/tomduck/myiapws/master/images/coexistence-curves.svg)
