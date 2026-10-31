# Dual-Op Trainer

A browser simulator for practising dual-operator car shots on a DJI Inspire 3. You can take the camera operator's seat on the gimbal, the pilot's seat on the aircraft, or both at once with two controllers. Shots are scored on framing, smoothness, holding the line and keeping clear of the car. There are also drills: a hover box in A mode, a nose-forward figure 8, a nose-in orbit, and a camera-op drill that holds a fixed subject.

**Open it:** https://elliotharrison111-ai.github.io/dual-op-trainer/ in Chrome, Edge or Brave on a computer.

## Controllers

- **DJI RC 2 or RC Plus:** power the aircraft off and plug the controller in with a data USB-C cable. Then Controls → **Connect DJI controller (USB)** → pick it → **Stick setup**.
- **DJI RC-N1, RC-N2, RC-N3:** Controls → **Connect RC-N serial**.
- **Xbox and other gamepads, and RC transmitters in USB joystick mode:** plug in and press a button.
- Keyboard and mouse work without a controller.

Connect a second controller for the Dual seat and assign each one under Seats.

## Physics

Settings → Physics → **Physics v2 (beta)** turns on the newer flight model, which is still being validated:
- fixed 240 Hz steps;
- the aircraft tilts before it accelerates;
- yaw and climb are limited in acceleration and jerk;
- air thins with altitude;
- the AI pilot flies the same model.

It is off by default, and best scores are kept separately for v1 and v2. Wind with gusts, A (ATTI) mode and Cruise Control work in both.

## FPV mode

The **FPV Free Fly** card flies a 5-inch Betaflight quad, in Acro or Angle mode, on any location while the car drives its route.

1. **Connect a controller.** Plug an FPV radio in over USB and choose USB Joystick on the radio; the TBS Tango 2 and other EdgeTX or OpenTX radios work this way. A gamepad or the keyboard works too.
2. **Run Radio setup** in the FPV panel. It finds your channels and your arm switch.
3. **Enter your quad's numbers** in the same panel: the rates from Betaflight's Rates tab, the weight, the thrust to weight and the camera uptilt.

The rate maths and defaults are Betaflight's own. The airframe numbers are estimates until you set them to your quad.

## Locations

| Location | What it is |
|---|---|
| Practice valley | Made up |
| Big Sky, Montana | Lone Mountain Trail |
| Gallatin Canyon: Lava Lake | US-191 below Gallatin Tower and Skyline Arête, with 2 m lidar terrain around the crags |
| Downtown Bozeman | Main Street, with buildings |
| Moab: Pool Arch Canyon | The Pool Arch (Rock of Ages) canyoneering loop above Pritchett Canyon, with 2 m lidar terrain and pins for the arch (approximate), trailhead and exit; Kane Creek Blvd for car work |

Location → **Make a map** builds other US locations from public map data. The built-in maps are for rehearsal only: verify terrain, roads, buildings and airspace on site.

**Map data:**
- Elevation and aerial imagery: U.S. Geological Survey (3DEP, National Map).
- Roads and water: U.S. Census Bureau TIGER/Line.
- Building footprints in the Bozeman map: © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright), available under the [Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/).
- Building heights: measured from USGS 3DEP lidar (MT Statewide Phase 3, 2021).

The building layer in `maps/bozeman.json` is a derivative of OpenStreetMap data and is available under the ODbL.

Scores, takes and recorded shots stay in each person's browser. Not affiliated with DJI. Flight and gimbal behaviour is a training approximation; see the realism notes in the source repository for what is measured, published or estimated.
