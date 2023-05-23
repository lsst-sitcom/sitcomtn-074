:tocdepth: 1

.. sectnum::

.. Metadata such as the title, authors, and description are set in metadata.yaml

.. TODO: Delete the note below before merging new content to the main branch.

Overview
========

This document describes the procedure to pump and cool down LATISS from ambient pressure to its operational temperatures. 
It also outlines how to perform a controlled warm-up in the case of servicing or programmed power cuts. 

Pumping LATISS to vacuum
========================

Under atypical circumstances, LATISS needs to be warmed up to ambient temperature. 
Large periods of power outage, severe earthquakes (`and different levels of recovery based on severity <https://tstn-027.lsst.io>`__), or technical intervention may have necessitated warm-up.
Pumping down, cooling, and powering up LATISS takes at least two days, and must be organized by ticket on the summit calendar and supported by daytime engineering support. 
Mario Rivera, Craig Lage, and Alysha Shugart are points of contact for understanding and initiating the procedure. 

Getting started
---------------

AuxTel must be under LOTO or the `E-STOP <https://obs-ops.lsst.io/Daytime-Operations/Auxiliary-Telescope/AuxTel-E-Stop-Procedure/E-Stop-Procecure.html>`__ must be engaged to perform this operation. 
The safety team is responsible for the the approval of the LOTO procedure, which will be linked on this page once it is affirmed.
 
Start by powering up the instrument cooling electronics, located in the first floor cabinet. 
It is important to make sure that the electronics are turned on but the outputs are disabled, so no control loops are operating on LATISS until it's under vacuum. 
These electronics consist of:

-  3 HMP2030 power supplies
-	1 Keithley 6487 Voltage Source
-	1 Advantech Uno-1483G-434AE rail controller (not used in the process)
-	1 Cryocon temperature controller (for CCD sensor)

.. figure:: /_static/power_supply_picometer.png
   :name: power-supply-picometer
   :alt: Power supply picometer

   HMP2030 Power Supply (left) and Keithley 6487 Voltage source (right).

.. figure:: /_static/rail_and_cryocon_controller.png
   :name: rail-and-cryocon-controller
   :alt: Rail and cryocon controller

   Advantech Rail controller (left) and Cryocon Temperature controller (right).

Setting up the turbo (vacuum) pump
----------------------------------

The spectrograph needs to work in a good vacuum (~10−7 Torr). For reaching this vacuum, there are two devices involved:

-	Pfeifer Turbopump (to be used from 1 Torr to ~10−6 Torr), complete with vacuum hose, pressure sensor and the sensor’s electronic display

-	Ion pump (to be used from 10−6 Torr onwards)

.. figure:: /_static/turbo_pump_equipment.png
   :name: turbo-pump-equipment
   :alt: Turbo pump equipment

   Pfeifer turbopump and accessories.

The Pfeifer turbopump lives in the AuxTel storage container on Calibration Hill. 
The turbo pump, vacuum hose, power supplies, and pressure sensor are stored together on the floor and first shelf of the storage container. 
The cardboard storage box is labeled. 
The key to the storage container is found in the key box on the second floor (control room floor) of the main building, to the right of the main entrance doors. 
Mario Rivera also has a copy. 

.. figure:: /_static/auxtel_storage.png
   :name: auxtel-storage
   :alt: Auxtel Storage

   Turbo pump supplies located in the storage unit outside of the AuxTel dome.

The ion pump (mounted on LATISS) doesn’t have enough capacity to evacuate the dewar from normal atmospheric pressure to working pressure, so the Pfeifer Turbopump has to be used first. 
The ion pump should be started only after ~10−6 Torr is reached (as the high pressure could destroy the ion pump).

Connect the turbopump to the dewar
-----------------------------------

Put the turbopump in a stable position close enough to the dewar position (to be close to the flange connections). 
An example setup is shown in Figure 5. 

.. warning::
   The Pfeifer Turbopump must be supported on a stable surface and strapped to the observing deck grating to ensure its safety in the case of an earthquake. 
   The turbopump's operation is degraded if it is not operating on a secure surface.
   A stout stool can be found on the observing floor of AuxTel which is perfect for this setup. 
   It is likely that the instrument will need to be rotated to +20 degrees to accommodate this. 
   The telescope mount may also need to be rotated to accommodate all of the power supplies necessary to run the turbopump and vacuum sensors.

.. figure:: /_static/turbopump_setup.png
   :name: turbopump-setup
   :alt: Turbopump setup

   Left - Connecting the turbopump to the dewar. Right - Vacuum hose connection to the dewar. 

Remove the vacuum covers, and clean the turbopump and the hose flange with isoporpyl alcohol (using gloves), to avoid introducing contaminants inside the turbopump and hose.
Connect the hose to the turbopump flange. 
The hose has to be in a relaxed shape, with no turn or folds. 

After checking the instrument dewar valve is closed, clean both the vacuum hose and instrument dewar flange with alcohol.
Connect the other end of the hose to the dewar, without forcing the hose into a stressed position.
This is why it may be necessary to rotate Nasmyth #2 between 0° and 20° to find a comfortable fit. 

Check the turbopump output valve is closed.

.. figure:: /_static/instrument_dewar_valve.png
   :name: instrument-dewar-valve
   :alt: LATISS dewar valve

   Picture of the LATISS dewar valve. 

.. note:: 
   The turbopump pump output valve is not typically used during the procedure. 
   What is important is that the pressure in the vacuum line to be lower than the pressure of the dewar BEFORE opening the dewar valve. 

Starting the turbopump
----------------------

Connect the external pressure sensor to the turbopump. 
This is an external sensor that is mounted on the top of the turbopump, and connects to an electronic display. 
See figure 7.
This pressure sensor is identical to the dewar pressure sensor on the first floor. 
To start the electronic display read out, press and hold the up arrow key for three seconds.

.. figure:: /_static/pressure_sensor.png
   :name: pressure-sensor
   :alt: Turbopump pressure sensor

   Left – Turbopump vacuum line sensor (connected to the top of the pump). Right – Pressure electronic display.

.. note::
   The setup in the left photo of Fig. 7 is example only. 
   Please do not operate the Turbopump on a non-rigid surface. 

Connect the turbopump to a secure electrical outlet, and turn the flip switch (at the back of the device on the lower right) to turn the pump on.
This only puts the pump in operational condition, it’s not evacuating air yet.

Start the pump (with the front power button). 
The turbopump will spin up to 1500 Hz in full operation.

.. figure:: /_static/operational_turbopump.png
   :name: operational-turbopump
   :alt: Operational turbopump

   Turbopump is fully spun-up.

Before opening the instrument dewar valve, it’s necessary to have similar vacuums on the pump and inside the dewar. 
If this is not the case, the turbopump or the dewar inside LATISS could receive a high pressure shock. 
Ideally, you should wait until the pressure is lower on the turbopump's side.

- If the dewar was evacuated completely, its pressure should be close to the turbopump at this point (~ atmospheric pressure).

- If the dewar was partially evacuated, it could have a pressure lower than atmospheric (e.g. ~10−3 Torr).

In any case, the pressures on both the pump and the dewar should be on the same order of magnitude before opening the dewar valve. 
If the dewar pressure is ~10−3 Torr, open the dewar valve only when the pump pressure is lower than ~10−3 Torr. 

.. warning::
   The process to open the dewar valve should be very slow. 
   Keep an eye on the pressure of the vacuum line. 
   Upon opening the dewar valve, the pressure in the vacuum line will spike. 
   Close the dewar valve again until the pressure settles, and slowly reintroduce the pressure differential. 

Starting the ion pump
---------------------

The turbopump should have reached a pressure of about ~10−5 Torr. At this point, you can start the ion pump.
The ion pump is on the instrument mount itself, hanging upside down. 
To turn it on, simply flip the switch on the front of the box. 

.. figure:: /_static/ion_pump.png
   :name: ion-pump
   :alt: LATISS ion pump

   LATISS ion pump.

Leave the turbopump running in case there is a pressure spike. 
The turbopump can help compensate for some outgassing events that will happen. 

Turn on and off the ion pump several times and watch the dewar pressure burp. 

When the ion pump comes on and settles into operations, there is an outgassing event. 
This is seen in figure 10 at 1355 UTC. 
Wait to close the dewar valve until this outgassing event has stabilized and the dewar and turbopump pressure reach similar values again. 

.. figure:: /_static/outgassing.png
   :name: outgassing
   :alt: Ion pump outgassing

   Ion pump outgassing event at 1355.

The current on the ion pump is an indication of how hard it is working. 
In normal operations, the only LED that should be visible is the HV Bias LED. 
If any other LEDs are lit, the ion pump is working too hard. 
See figure 11. 

.. figure:: /_static/ion_pump_normal.png
   :name: ion-pump-normal
   :alt: LATISS ion pump at normal ops

   LATISS ion pump at normal operations. HV Bias LED is lit at the bottom.

Once the ion pump is operating normally and there are no more pressure spikes, the dewar valve may be closed and the turbopump turned off. 

To turn off the turbopump

   -  Close the LATISS dewar valve. This will protect the dewar from the increase in pressure in the vacuum line.
   -  Press the button on the front of the turbopump. 

After the frequency goes down from 1500 Hz to 0 Hz, it’s possible to completely turn off the pump (flipping the back switch).
Verify that the pump blades are not spinning (this could take some time, as it doesn’t have a brake).

.. note:: 
   It is good practice to leave the turbopump connected to the instrument dewar just in case it is needed to pump further. 
   Only disconnect the turbopump when you have the CCD cooled to operating temperature and the cryogenic control loops in place.

Set up the cryogenics
---------------------

Once the dewar pressure is reaching 10-7 Torr, it’s time to start the cryogenics devices, to start controlling the dewar temperatures. 
For this, we have these devices:

-	Polycold Cryochiller
-	Cryocon 24C unit, for temperature monitoring

The Cryocon controls the temperature of:

-  CCD stage, which is reported on Channel A. The set point is 179K.
-  Cryohead which is reported on Channel B. The set point is 126K.
-  Cold plate which is reported on Channel C. The set point is 158K.

.. note::
   An important point to note is the CCD stage must always be the warmest device - at least 3K higher than the cold plate - to avoid condensation.
   This is especially important when warming the dewar (as the Cryohead and Cold plate tend to warm faster than the CCD stage).

For setting the control temperature loops, the Cryocon uses Channels A (CCD Stage), B (Cryohead) and C (Cold plate).
The control loop setup (for cooling down the temperatures in a controlled way) is done through the ‘’Loop’’ buttons (1 and 2).

.. figure:: /_static/cryocon.png
   :name: cryocon
   :alt: Cryocon

   Cryocon temperature controller display and panel. Located on the first floor in the large electronics box.

The normal setup parameters should be stored on the device. 
You may find an example setup screen in Fig. 13. 

To set up the Cryocon, the steps are:

- Check the above parameters (shown in Fig, 12) for Loop 1 (CCD stage).
- Verify that “SetPt” = 179K.
- Check the above parameters for Loop 2 (Cold plate), with ‘’SetPt’’= 158K, and ‘’Type’’ = Manual
- Press the ‘’Control’’ button, and verify the indicator appears blue.

**In case the values are not correct, or the heater power needs to be changed, you must manually enter the values you want.** 
   
- Press the “loop 1” button to enter the settings panel for the CCD stage. 
- Use the arrow keys to navigate to the value you want to change,
- For example, to change Pman from 15% to 1%, press the arrow keys until the # sign is next to the value.
- Press the “SetPT” button to change the value.

   - The first time you hit the “SetPT” button, the value will change to “-“.
   - Hit “SetPT” button again to clear the field, and use the number pad to enter a decimal value. 

- Hit “Enter” to save the new value.

.. figure:: /_static/cryogen_settings.png
   :name: cryogen settings
   :alt: Cryogen settings

.. figure:: /_static/cryogenic_loop1.png
   :name: cryogenic loop 1
   :alt: Cryogenic settings for loop 1

   Nominal values for Channels A, B, and C, as well as loop 1 and loop 2 settings. 

Turn on the Polycold
--------------------

After the above steps, it’s time to turn on the Polycold, which is located just to the left of the large electronics cabinet. 
For this, just press the start switch.

After all the above steps, the temperatures should start to go down in a controlled way, until the CCD stage reach the desired setpoint (179K). 
It will take several hours to cool down, so this process should require an overnight stay or monitoring. 
After that, the Cryocon will start controlling automatically.

Checking the cryocon status remotely with CCS
---------------------------------------------

Log in to the machine with ssh -XY <username>@auxtel-mcm.cp.lsst.org.

Type ccs-shell at the prompt.

This will put you in the CCS shell to allow running CCS commands.

ccs>set level ats 1

ccs>switchToEngineeringMode

Now you are in engineering mode and can see the CryoCon commands.

ccs>ats/ <TAB> will show the available modules, as follows:

   | ats/TempCryoHead 
   | ats/periodicTasks 
   | ats/CryoCon 
   | ats/TempCCDSetPoint 
   | ats/Vacuum 
   | ats/MonitorControl 
   | ats/TempColdPlate 
   | ats/TempCCD ats/Pfeiffer

ccs>ats/CryoCon get <TAB> will show the available data, as follows:

   | getSubmittedChanges 
   | getUnit
   | getMaxSetPoint 
   | getSetPoint 
   | getHtrRead 
   | getPidP 
   | getPidI 
   | getPidD 
   | getLoopSource
   | getHeaterRange 
   | getHeaterMax 
   | getTemp 
   | getOtdSource 
   | getOtdTemp 
   | getControlType 
   | getHeaterPower 
   | getType

There are two control loops, so you need to enter the number of the loop. For example:

ccs>ats/CryoCon getPidP 1

will return the PidP parameter for loop 1, which should be 0.1.

ccs>ats/CryoCon getHtrRead 

reads the current heater power output, which is useful to know.

ccs/>CryoCon isInControl  

will tell you if the CryoCon is controlling.
This is equivalent to the blue light on the front panel.

ccs>CryoCon setToControl  
will turn on the control if it is not controlling.

In the future, we will be able to adjust the CryoCon parameters using CCS, but this capablility is not available yet.

Power up the CCD
----------------

The full process to power up or power down the CCD is described in this `technote <https://sitcomtn-026.lsst.io/>`__. 

Temporary Shutdown
==================

In normal operations, the spectrograph should not be shut down in any way, given the CCD stage needs to be maintained at a specific temperature (and always warmer than the Cold plate). 
In case an electronics shutdown needs to be done for maintenance or other matters (for a short time), follow this procedure:

- Adjust the Loops 1 (CCD stage) and 2 (Cold plate):

   -	In Loop 2, reduce ‘’Pman’’ to 10%

   -	In Loop 1, change ‘’Type’’ to ‘’Manual’’

   -	Press ‘’System’’ -> ‘’OverTemp Configuration’’ and set the next parameters: 
      
      - ‘’OTD Enable’’=On, ‘’OTD Source’’ = Channel A, ‘’OTD Setpoint’’ = 293K


- Turn off the Polycold Cryochiller

   -  Now, the dewar will start to warm up (as Polycold is off). 
      The key here is to keep an eye on the CCD stage temperature, as it always has to be warmer (by at least 3K) than the Cold plate. 
      To manage this, the parameter to be controlled is ‘’Pman’’ (it should be 15% by default).

   -	If the difference between the CCD stage and the Cold plate gets close to 3K, increase ‘’Pman’’ a bit (from 15% to 16% e.g.). This will increase the CCD stage heater, and then the CCD will be warmer than the Cold plate.

   -	After a while, the temperature difference will start to equalize again, so ‘’Pman’’ should be changed again (to 16.5%-17%).

   -	The warming up process should be slow, so increasing Pman to higher values to accelerate the warming rate is not recommended. Pman should be around 15%-18%.


As said before, it’s important to keep monitoring all the time that CCD stage is always warmer than Cold plate (by at least 3K).
After CCD stage reaches the Overtemp setpoint (293K), the Cryocon will start controlling, and it will shut itself down. 
The full process takes about 6 hours.

Complete warm up
================

This process overviews the process for a controlled warm up in case the instrument or telescope needs servicing.
In case of a unexpected power cut (storm or large earthquake), if LATISS goes into an uncontrolled warm up, follow `this procedure <https://tstn-027.lsst.io/>`__.  

- `Power down <https://sitcomtn-026.lsst.io/>`__ the CCD, but leave the cryocon turned on.

- Hook up the turbopump, but leave the instrument valve closed!

- Start pumping on the turbopump vacuum line.

- Pump it down until the turbopump reaches the order of 10-7 torr.

	- This takes several hours, so this process should be initiated at the beginning of the day.

- When the turbopump reaches the approximate pressure of LATISS, turn off the ion pump. 

- Open the instrument valve SLOWLY - have the CCS monitor or chronograph open and watch the pressure inside the instrument, as well as the turbopump pressure monitor. 

- Once the instrument valve is open, go downstairs and turn off the Polycold chiller. 
  There is a rocker switch to turn it off. 

- Then watch the pressure/temperature as it warms up. 
  The pressure will climb pretty high, maybe even up to 10-4. 

- As it warms up, watch the temperatures and make sure the CCD isn't the coldest thing in the instrument. 
  This is where you need to intervene with the cryocon (see sections 2.6 and 3). 
  Add heat to the CCD if it's getting too cold. 
  This is a process of trial and error. 


.. Make in-text citations with: :cite:`bibkey`.
.. Uncomment to use citations
.. .. rubric:: References
.. 
.. .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib
..    :style: lsst_aa
