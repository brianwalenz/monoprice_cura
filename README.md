[Cura 2.6](https://ultimaker.com/en/products/cura-software) configuration file
and profiles for the [Monoprice Select Mini
v2](https://www.monoprice.com/product?p_id=21711) 3D printer.

Adds a "Monoprice Select Mini" printer configuration to the "Other" machines in
the "Add Printer" dialog.

Adds seven profiles specific to the Mini to the print profiles list.

| Layer Height  | Name       | Options
|---------------|------------|-------------------------
| 0.04375       | ExtraFine  | Infill layer height x4 = 0.175
| 0.0875        | Fine       | Infill layer height x2 = 0.175
| 0.13125       | Decent     | Infill layer height x2 = 0.2625
| 0.175         | Normal     | 
| 0.21875       | Draft      | 
| 0.2625        | Coarse     | 
| 0.30625       | ExtraCoarse| 

* The ExtraFine setting is **very** tiny.  Print times on
  [3DBenchy](https://www.thingiverse.com/thing:763622) went from 1:45 with
  'Normal' to 9 hours with 'ExtraFine' -- and it had bed adhesion problems.  The
  railing on Benchy was quite nice though.

* The ExtraCoarse setting will move a lot of plastic.  Hot end temperature might
  need to be increased a bit.

* Infill layer height, especially on ExtraFine, is not tested.

* Retraction for all is set to 3mm at 40mm/sec.  This might be a tad too small.
  I haven't tested it much.

## Installation

1. Install [Cura](https://ultimaker.com/en/products/cura-software).
2. [Download](https://github.com/brianwalenz/monoprice_cura/archive/master.zip) this package.
3. Unzip the package.
4. Double-click on 'install'.

Only supported on Mac OS.  The config files probably are platform independent,
but I don't know where they go on other platforms.

## Credits

* Michael O'Brien discovered the layer heights, see his
  [hackaday](https://hackaday.io/project/12696-monoprice-select-mini-electro-mechanical-upgrades)
  project, specifically his [exploration of the
  motors](https://hackaday.io/project/12696-monoprice-select-mini-electro-mechanical-upgrades/log/44772-x-y-z-a-motors-stepper-driver-investigation),
  for all the gory details.

* Tyler Gibson has a [readable
  explanation](http://www.thetylergibson.com/monoprice-select-mini-part-3-tuning-and-slicing/)
  of these settings.  Ignore the PID tuning sections, the v2 doesn't need them.
  Start at "Slicing with Cura", about half way down.

* Azim Sonawalla's
  [monoprice_cura](https://github.com/asonawalla/monoprice_cura) was the seed
  for this repo, specifically, the path to the config file.
