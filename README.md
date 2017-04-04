# CO2LaserSchematic
Laser controller board with 32-bit main processor and integrated 16-bit PPI-processor subsystem

**Hardware:**

1. Main board

* 3-axis motion controller for four motors, Y-output is switchable between two motors \(Y or A\).

* Texas Instruments \(TI\) Tiva TM4C123GH6PM as main processor - ARM Cortex M4F: 80 MHz, 256 KB flash, 32 KB SRAM, 2KB EEPROM, ROM-based driver library \(TivaWare\).

* TI MSP430G2553 MCU in combination with two CPLDs provides PPI-control for lasers, controlled by main processor via I2C.

* Isolated input via USB-to-serial \(FT232RL\)or direct serial provided by an ADUM1402, optionally USB directly \(not isolated\).

* I2C bus made available for add-on boards.

* On board regulator for +5V and +3.3V, 6.5 - 36 V supply range

2. Relay control board

* via I2C - for air assist, coolant pump and fans, 4 channels available. Includes support for coolant flow detection.

3. Front panel boards

* Control via I2C, for display and buttons. Board made with OLED display for status, 13 buttons for power, relay control, laser test fire and axis jogging.

**Firmware/software:**

* Proprietary code for engraving, supporting desktop application written in C# for Windows.

* Mach3 option via piggyback to common paralell port breakout board, supported in proprietary code \(mode select\).
PPI mode available, controlled by desktop application.

* Grbl option, code has been ported from version 1.1f - is integrated with proprietary code \(mode select\).
Grbl port is HALified; driver supports jogging, power setting/override and coolant control via front panel buttons.


More info over at [buildlog.net](http://www.buildlog.net/buildlog/view_log.php?id=2625&dir=asc)

A [YouTube]( https://www.youtube.com/watch?v=nkeuVN_bmTo&t=1s) video showing my laser cutting a mylar PCB stencil.
