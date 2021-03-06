.. _motor-thrust-scaling:

====================
Motor Thrust Scaling
====================

Copter includes *motor thrust scaling* which compensates for the
non-linear thrust output of most ESCs and motors. 

.. tip::

    The default curve should work for nearly all ESC/motor combinations. 
    Normally the parameters should not be adjusted unless the vehicle’s actual 
    thrust curve has been measured.

.. note::

    Motor thrust scaling was introduced in Copter 3.3.

Thrust Curves
=============

The curve is controlled by two parameters:

-  **MOT_THST_EXPO** controls the shape of the thrust curve with "0"
   meaning a completely linear curve and "1.0" being very curved (see
   pictures below).  The default is "0.65" (the image below incorrectly
   states the default is 0.5).

.. image:: ../images/MotThstExpo_graphs2.png
    :target: ../_images/MotThstExpo_graphs2.png

-  **MOT_THST_MAX** controls the point at which the thrust flattens
   out near it's maximum.  By default this is 0.95 meaning 95% of full
   throttle.

Thrust Stands
=============

The thrust stands listed below can be used to measure the PWM signal vs thrust output for a vehicle's specific motor, esc and battery

- `RCbenchmark.com thrust stands <https://www.rcbenchmark.com/pages/series-1580-thrust-stand-dynamometer>`__
- `Turnigy thrust stand <https://hobbyking.com/en_us/turnigy-thrust-stand-and-power-analyser-v3.html>`__

Parameter Calculation
=====================

A copy of this spreadsheet can be used to calculate the appropriate values from the thrust stand data above:

https://docs.google.com/spreadsheets/d/1_75aZqiT_K1CdduhUe4-DjRgx3Alun4p8V2pt6vM5P8/edit#gid=0

