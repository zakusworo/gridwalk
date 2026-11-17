# How to use Gridwalk

Each tool has a **?** button in its title bar that opens its guide. Load the examples first (Settings → Examples → Load examples) to try every tool with ready-made records.

## Site details
A site is one project location: a roof, a river, a wind site, a geothermal field, a farm.
1. Name it and tick its energy sources. The colour dots stay with each source everywhere in the app.
2. Stand on the site and tap **Use my position**, or type the coordinates. The position is needed for resource data and sun paths.
3. Fill in the survey notes: structure, access, grid connection point and meter number.
4. Save. The site opens on the Sites tab; fetch its NASA POWER data there.
- Moving a site's position clears its resource data, so fetch it again for the new point.

## Meter readings
1. Name the meter (for example "Inverter 1" or "PLN export") and pick what it counts.
2. Read the cumulative register and save. The energy per day appears once there are two readings.
3. **Export CSV** shares the readings.
- A reading lower than the last one is refused: a replaced meter gets a new name.

## Wind readings
1. Hold the anemometer at a fixed height away from buildings and trees, and type the speed and height.
2. Face into the wind and tap **Point into wind** to record where it comes from.
3. After three readings the app shows the mean, a Weibull fit, power density and the speed at 30 m.
- Spot readings are a first look only. A project needs a season or more of mast data.

## Head survey
Gross head for micro hydro, by levelling down the penstock route.
1. Start at the intake. Sight to the next point at the same eye height and read the angle down (Abney level or the clinometer).
2. Measure the slope distance with a tape and tap **Add leg**. Move to that point and repeat down to the powerhouse.
3. Head = Σ distance × sin(angle). Optionally mark the intake and the powerhouse with GPS as a rough check.
4. Save the survey; it shows on the site dashboard.

## Shading survey
Trace the skyline from the array position to see which months lose direct sun.
1. Stand where the array will be. Aim the crosshair at the top edge of each obstacle (tree, roof, hill) and tap **Add point**, sweeping across the sun's side of the sky.
2. Tap **Done tracing**. The sun-path diagram shows every month's path; where a path runs under the grey skyline, that month loses direct sun at those hours.
3. Enter the panel tilt and the direction it faces to get the monthly and yearly loss.
4. Name the survey and save it. Tap a saved survey to load it again.
- Calibrate the compass first (figure 8) and keep away from steel roofs and cars: azimuth errors move the whole skyline.

## Panel tilt and azimuth
Lay the phone on a panel (or on the roof where panels will go).
1. Lay the back of the phone flat on the panel surface.
2. **Dip** is the panel tilt; **dip direction** is the way the panel faces (true north with a GPS fix).
3. Tap **Hold reading** before lifting the phone.
- Use these two numbers in the yield estimate and the shading survey.

## Inspections {#P2H}
PV commissioning, small wind, micro hydro, battery room, work at height and electrical isolation (LOTO).
1. Tap **New inspection** and pick the checklist.
2. Name the site or equipment and who inspects.
3. Answer every item **OK**, **Defect** or **N/A**; describe each defect.
4. Save. A failed critical item makes the verdict **Not ready**.
5. Open an inspection to share it as a PDF with signature lines.
- The PV list follows the items IEC 62446-1 asks for; it does not replace the test report the standard requires.

## Sites
The dashboard of the site you are working on.
1. Tap **All sites** (or **Change site**) under the site name to switch sites or add one. Each site in the list shows its 12-month curve.
2. With no resource data yet, tap **Fetch NASA POWER data**: monthly sun, temperature and wind for the site's position (needs internet once).
3. Tap a bar in the chart to read that month; **Values** shows the table. Solar sites chart sun; wind-only sites chart wind at 50 m.
4. **Logged at this site** lists its meters (with energy per day), wind readings, head and shading surveys.
5. **Tools for this site** lists the calculators for its energy sources.
- Load the examples (Settings → Examples) to see five sites with data.

## Tools
Every tool, grouped by energy source.
1. Tap a source chip to see only its tools, **All** for everything, or **Electrical, units** for cables, fuses, money and units.
2. Field tools (shading survey, panel tilt, sun position, wind readings, head survey) sit at the top of their source.
3. Every calculator has two worked examples and its own guide behind the **?** button.

## Map
Sites, tracks and imported maps.
1. Sites show as dots in the colour of their first energy source.
2. Use the buttons on the right to measure, open the map library, centre on your position or import a file.

## Logs
Readings, surveys, inspections, reports and field instruments.
1. **Meter readings**, **Wind readings**, **Head surveys** and **Shading surveys** belong to the active site.
2. **Inspections** and **Daily report** cover the visit; both share as PDF.
3. GPS camera, tracks and compass are here for site work.

## Load audit
1. Type one load per line (or separate with ';'): watts, hours per day, quantity. For example `10 6 8` is eight 10 W lamps for 6 hours.
2. Set a design margin.
3. Read the daily energy (with and without margin) and the peak load if everything runs at once.
- Measure fridge and pump hours: they cycle, so nameplate × 24 h overstates them.

## PV array size
1. Enter the daily energy needed and the peak sun hours of the worst month (the lowest monthly GHI from the site's data).
2. Keep the performance ratio near 0.75 for grid-tied, lower (0.6–0.7) for off-grid with batteries.
3. Read the array size and the number of modules.

## Yield estimate
1. The monthly GHI and latitude come from the active site; change them for another place.
2. Enter the array size, tilt and the direction the panels face (0 = north, 90 = east).
3. Read annual energy, specific yield, the plane irradiation and the best and worst months.
- Near the equator a small tilt (10–15°) mainly helps self-cleaning in the rain; the gain is small.

## String sizing
1. Copy Voc, Vmp, Isc and the temperature coefficients from the module datasheet.
2. Enter the coldest morning temperature and the hottest afternoon at the site.
3. Enter the inverter's maximum DC voltage, MPPT range and maximum input current.
4. Read the allowed modules per string and the parallel strings per MPPT.
- Highland sites have cold mornings: that is what limits the string length.

## Inverter sizing (DC/AC ratio)
1. Enter the array size (kWp) and the inverter AC rating.
2. Read the ratio and whether it is in the usual range.

## Row spacing
1. Enter the latitude, the panel's slope length, the tilt and the earliest solar hour that must be shade-free.
2. Read the row pitch, the gap between rows, the ground cover ratio and the sun's position at that time.
- Solar time differs from clock time by up to an hour in Indonesia; check with the sun position tool.

## Measured vs datasheet
1. Measure the string's Isc and Voc, and at the same moment the plane irradiance and the cell temperature.
2. Enter the datasheet Isc, Voc, the number of modules and the coefficients.
3. Read both values at STC and how far they are from the datasheet.
- Measure above 700 W/m² in steady sun; a string more than 5 % low needs a closer look.

## Performance ratio
1. Enter the energy delivered in a period, the array size and the irradiation on the panel plane over the same period.
2. Read PR, final yield and reference yield.

## Wind speed at hub height
1. Pick power law or log law.
2. Enter the measured speed, its height and the hub height, plus α or the roughness length.
3. Read the speed at the hub and the power ratio.

## Wind power density
1. Enter the mean speed at the height of interest.
2. Give the spread as a Weibull k, or as the standard deviation of your readings.
3. Enter the site altitude and temperature for air density.
4. Read the power density, Weibull k and c, and the air density.

## Turbine energy yield
1. Paste the turbine's power curve as speed-kW pairs from its datasheet.
2. Enter the mean speed at hub height, Weibull k, air density and availability.
3. Read the annual energy and, with the rated power, the capacity factor.

## Stream flow: float method
1. Mark a straight reach (10 m or more); time a float over it several times and average.
2. Measure the channel width and mean depth.
3. Keep k = 0.85 for a smooth bed (lower for rough, shallow streams).
4. Read the flow.
- Measure in the dry season for the design flow of a run-of-river plant.

## Weir flow
1. Pick V-notch or rectangular.
2. Measure the head above the crest a few notch-widths upstream.
3. Read the flow.

## Flow: bucket method
1. Channel the whole flow into a container of known volume.
2. Time several fills and type the times separated by spaces.
3. Read the flow in L/s and m³/h.

## Hydro power and turbine
1. Enter the design flow, net head and overall efficiency.
2. Optionally enter the turbine speed for the specific speed.
3. Read the power, annual energy at the capacity factor given, and the suitable turbine types.

## Penstock
1. Enter flow, inside diameter, length, gross head, material, wall thickness and roughness.
2. Read velocity, friction loss (also as % of head), net head, wave speed and the surge for an instant closure.
- Close valves slowly: the surge figure is the worst case.

## Geothermometers
1. Enter the water analysis of a hot spring: SiO₂, Na, K and Mg in mg/kg (any you have).
2. Read the silica and cation temperatures.
- Only near-neutral chloride waters in equilibrium give a reservoir temperature; check them on a Na-K-Mg diagram first.

## Steam tables
1. Pick pressure (bar abs) or temperature (°C) and type it.
2. Read saturation temperature or pressure, enthalpies, entropies and specific volumes.

## Flash: steam and brine split
1. Give the fluid enthalpy: from the reservoir temperature (liquid well) or measured.
2. Enter the separator pressure and, optionally, the total well flow.
3. Read the steam fraction, separator temperature, and steam and brine flows.

## Well output: lip pressure
1. Enter the discharge pipe ID, the lip pressure and the discharge enthalpy.
2. Optionally enter the separator pressure for the steam split.
3. Read the total mass flow and the steam at the separator.

## Plant output
1. Enter the steam flow, turbine inlet pressure, condenser pressure and turbine-generator efficiency.
2. Read gross MW, the isentropic drop, the specific steam consumption and the exhaust dryness.

## Battery bank
1. Enter the daily energy taken from the battery, days of autonomy and bank voltage.
2. Pick the chemistry (sets the usable depth of discharge) and the efficiency.
3. Enter one battery's voltage and capacity.
4. Read the capacity needed and how many batteries in series and in parallel.

## Charge controller
1. Enter the array's total Isc, its power and the battery voltage.
2. Read the minimum rating for a PWM and for an MPPT controller.

## Biogas digester
1. Enter the fresh feed and water added per day, total solids and volatile solids.
2. Enter a biogas yield per kg VS (measure or use local data), retention time and methane content.
3. Read digester volume, biogas, methane, energy and organic loading.

## Biogas to power
1. Enter the biogas per day, its methane content, the generator efficiency and running hours.
2. Read the electricity per day, the generator size and the heat available.

## Biomass fuel
1. Enter the dry heating value, the moisture (wet basis) and the conversion efficiency.
2. Read the heating value as received and the fuel needed per kWh (and per day if you give the energy).

## Cable size by voltage drop
1. Pick DC/single phase or three phase, then enter voltage, current, one-way length and the allowed drop.
2. Pick copper or aluminium and the conductor temperature.
3. Read the minimum cross-section, the next standard size and the drop with it.
- Check the current rating in the PUIL / IEC tables for how the cable is installed.

## PV fuses and breakers
1. Enter the module Isc and its maximum series fuse rating.
2. Optionally enter the inverter's maximum AC output current.
3. Read the string fuse window, a standard fuse in it, and the AC breaker size.

## Power, current, voltage
1. Pick DC, single phase or three phase and enter voltage, current and power factor.
2. Read real, apparent and reactive power.

## Payback and LCOE
1. Enter the investment, yearly O&M, first-year energy and the value of a kWh, all in one currency.
2. Enter the discount rate, lifetime and yearly degradation.
3. Read the LCOE, the simple payback and the net value per year.

## CO₂ and diesel avoided {#CALC_co2}
1. Enter the renewable energy per year.
2. For grid sites, enter your grid's current emission factor; for diesel sites, the genset's kWh per litre and the fuel price.
3. Read CO₂ avoided, diesel avoided and the fuel cost saved.

## Energy unit converter
1. Pick the quantity, type the value and pick its unit.
2. Read it in every unit of that quantity.

## Coordinate converter
1. Pick lat/lon, UTM or TM-3, or tap **Use my position**.
2. Read lat/lon, DMS, UTM, TM-3, grid convergence and magnetic declination.

## Distance and bearing
1. Enter two points' eastings and northings (and elevations if known).
2. Read distance, bearing, slope distance and gradient.

## Heat stress
1. Enter air temperature and humidity.
2. Read the heat index, its band and the shade WBGT estimate.
- On a roof in full sun the WBGT is several degrees higher.

## Lightning distance
1. Count seconds from flash to thunder; enter it with the air temperature.
2. Read the distance. Under 30 seconds, come off the roof or the tower.

# Shared tools



Guides for the tools every field app carries. An app's own tutorials.md overrides any section by key.

## Map
Everything you have switched on, drawn over the street map or your offline basemap.
1. Tap **+** to import a survey file, or the **folder** button to open the map library.
2. Tap the **target** button to centre on your position. Your position shows as a blue dot with a heading cone.
3. Pinch to zoom, drag to pan, and rotate with two fingers.
4. To measure, tap the **ruler** button, then tap points on the map. The panel shows distance, the last leg and its bearing, and the area once you have three points. Use **Undo**, **Clear**, or **Done** to finish.
- Layers are switched on and off in the map library, not on the map.
- With no signal the street map stays blank. Import an MBTiles or PMTiles basemap to work offline.

## Map library
All your maps, kept on the phone.
1. Before importing files in metres (DXF, STR, projected CSV), set the **Default UTM zone** to the zone of the file, for example 48S for West Java or 50S for East Kalimantan.
2. Tap **Import** and pick a file. Supported: DXF (lines, polygons, points, 3DFACE TINs), Surpac STR, KML, CSV (P,N,E,Z,D or lat/lon), GeoPDF, plain PDF drawings, and MBTiles or PMTiles raster basemaps.
3. Use the switch to show or hide a map. **View** zooms the map to it. A plain PDF opens as a document instead.
4. The **⋮** menu lets you rename the map, change its UTM zone, open a PDF as a document, or delete it.
- Deleting a map removes the app's copy only. The original file is not touched.
- If a file lands in the wrong place, its UTM zone was wrong. Use **Change UTM zone** to fix it without importing again.

## GPS tracks
Record where you walked or drove, or the area inside a boundary.
1. Choose the accuracy limit, for example **±20 m**. Worse fixes are not recorded.
2. Tap **Record a traverse** for a line, or **Walk a boundary (area)** to measure an area.
3. Put the phone away. Recording continues with the screen off, and a notification shows progress.
4. Tap **Stop and save** and give the track a name. For a boundary, stop near your starting point: the area closes back to the first point.
5. Tap a saved track to show it on the map, export it as GPX, KML or CSV, rename it, or delete it.
- Standing still does not add points, so GPS wander does not grow the track.
- If the phone kills the app while recording, the track is saved as "Recovered …" the next time you open it.

## Compass
A sighting and walking compass that checks its own magnetometer.
1. Hold the phone flat with the bubble in the centre ring, then point the top edge. Read the heading under the index.
2. To sight a target, hold the phone upright and aim the back of the phone at it. The compass switches to sighting mode on its own.
3. **True north** needs a GPS fix (declination from the World Magnetic Model). Choose **Magnetic** to read the raw compass.
4. **Hold** freezes the reading. **Set target** marks the current bearing on the card and tells you to turn left or right to stay on line.
5. Read the box at the bottom:
   - **Calibrate:** wave the phone in a figure 8 until the accuracy reads high.
   - **Magnetic interference:** move away from vehicles, steel and pipework.
- The back bearing (+180°) is shown for back-sighting along a line.
- Check against the sun compass when the readings look wrong.

## Clinometer
Dip and dip direction of a surface, or the angle of a slope.
1. **Flat on surface:**
   - Lay the back of the phone on the surface. Any rotation works.
   - Read the dip in large digits, and the dip direction as the arrow against the compass ring.
2. **Edge along slope:**
   - Rest the long edge of the phone on the slope, lying flat or standing on its side.
   - Read the angle on the protractor, plus the grade and the 1 : n ratio.
3. Tap **Hold reading** to freeze the value before lifting the phone.
- On a surface too small for the phone, lay a clipboard on it and the phone on the clipboard.

## GPS camera
Photos stamped with position, bearing, time, address and a QR map link.
1. Wait for a GPS fix. The status line shows accuracy and satellites.
2. Tap the **pencil** to set the photo label and to switch the street address and the QR code on or off.
3. Aim and press the shutter.
4. Tap the thumbnail to open the photo log. From there you can show the photos on the map, export a CSV, or delete photos.
- Photos are saved in Pictures under the app's name, with GPS in the photo's EXIF data.
- The address needs signal. Offline, the stamp keeps the coordinates and UTM.

## Sun compass
Sun position, daylight, and a magnet-free check of your compass.
1. Read the sun's azimuth and elevation, sunrise, solar noon, sunset and the daylight left.
2. To check the compass:
   - Stand a pencil upright on a flat surface in the sun.
   - Lay the phone flat with its long edge along the pencil's shadow, top end pointing away from the pencil.
   - Read the **compass error**: within 3° is fine; more means calibrate, or there is steel nearby.
- The sun must be at least 8° up for a usable shadow.

## Calculator
1. Tap **Example 1** or **Example 2** to fill in a worked example, or type your own values.
2. Results update as you type. If something is missing, the result box says what to enter.
3. Read the formula and assumptions under the result before relying on the number.
- Choices such as methods or units are the chips above the input fields.

## Checklists {#P2H}
Inspections with a verdict: any failed critical item stops the job.
1. Tap the new-check button and pick the checklist.
2. Fill in what is being checked and who checks it.
3. Answer every item **OK**, **Defect** or **N/A**. For a defect, say what is wrong.
4. Save. The verdict is worked out from the critical items; there is no "all OK" button on purpose.
5. Open a saved check to share it as a PDF with signature lines, or export every check as CSV.

## Daily report
The day's report, half-filled for you.
1. Pick the day with the arrows.
2. **Recorded in the app** lists what was logged that day.
3. Tick the weather. Fill in the crew, hours, activities, hazards (incidents and near misses) and the plan for tomorrow.
4. Tap **Save report**, then **Share as PDF** to send it.
- Saved reports are listed at the bottom; tap one to open it.

## Settings
1. **Name** and **photo:** shown in the header, on GPS photo stamps and on imported maps.
2. **Theme:** Light, Dark, or follow the phone.
3. **Default UTM zone:** set it in the map library.
