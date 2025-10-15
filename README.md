# Zovious Wireframe Shooter

## Overview
Zovious Wireframe Shooter is an 80s-inspired forward-scrolling rail shooter built with WebGL and Three.js. Players pilot a neon vector fighter over stylised landscapes while dismantling hostile fleets and a looming fortress known as the Floating Citadel. The presentation fuses blueprint-style visuals, reactive synthesised audio, and lightweight HUD elements to keep the focus on high-speed action.

## Gameplay Loop
1. **Mission Start** – The title overlay introduces the sortie with a custom “ZOVIOUS” glyph logo and deployment prompt. Once activated, the craft launches immediately into Area 1.  
2. **Area Progression** – Each area extends for a long vector runway (doubled to emphasise endurance). Scenic objects and enemy squads are spawned via scripted map events tailored to the biome:
   - *Emerald Grove* – forest columns, agile scouts, light artillery.  
   - *Azure River Run* – hovering platforms, fast strafers, rippling grids.  
   - *Nazca Plateau* – monolith guardians, heavy bombers, converging fire lanes.
3. **Combat Rhythm** – The player can fire rapid aerial laser bursts and deploy ground-penetrating bombs. Maintaining shot cadence while evading bullet curtains increases survival odds and score.
4. **Fortress Encounter** – At the end of each area the Floating Citadel emerges. Turrets must be neutralised to expose the central core; a direct core strike instantly destroys the fortress, triggering a collapse cutscene.  
5. **Mission Complete** – After Area 3, an ending overlay fades in with the message “ALL OPERATE KGNINJA 2025,” acknowledging the strike team’s success.

## Controls
- `Arrow Keys` – Strafe the fighter within the forward corridor.  
- `Space` – Fire primary laser cannon (automatic cadence with cooldown).  
- `Z` – Drop a ground bomb toward the reticle impact point.  
- `F2` – Toggle debug invincibility (development helper).  
- `Mouse/Touch` – Activate the initial title overlay and unlock audio context.

## Audio & Atmosphere
- **Start Jingle** – An extended multi-chord synth flourish marks mission deployment.  
- **Background Arpeggio** – A gamelan-inspired triangle wave sequence loops with echo to build tension.  
- **SFX Palette** – Procedural buffers generate shots, explosions, fortress hum, and shield impacts, reinforcing the vector aesthetic.  
- **Ending Silence** – Background loops fade when the end credits overlay appears, accenting the completion message.

## Technical Notes
- Rendered with Three.js (`WebGLRenderer`) and line-based geometries to emulate vector displays.  
- Audio runs on the Web Audio API with lazy initialisation to satisfy browser gesture policies.  
- The world uses declarative “map events” so additional areas or enemy patterns can be slotted in without rewriting the core loop.  
- All overlays (title, HUD, ending) are DOM-driven, allowing rapid iteration of UI copy and styling.

## Credits
- Design, Programming, and Audio: **#KGNINJA Systems**  
- Narrative & Ops: **All Operate KGNINJA 2025**

Enjoy the flight, pilot. Stay sharp, keep the shield steady, and bring the fortress down in style.
