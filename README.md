# Puredata Patches

## Nudge and Clock from AbletonLink
### Setup
1. Install puredata (not plugdata - the AbletonLink external requires puredata). https://puredata.info/downloads
2. Install the abl_link~ External from inside Pd (deken is the package manager)
3. Create a folder for your patches.
4. Put the patch files all together in the folder.
5. Open the parent_for_link2clockNudge.pd patch.
6. Turn on Pd's DSP. If you are running an AbletonLink software, you should see the tempo of the Link session.
7. Setup Pd's MIDI Output. Select your MIDI Output device to send clock to.
8. Click Play. If the button in Pd doesn't click, press ctrl+E to swap in/out of Pd's edit mode.
9. The "Start Runs Clock" and "Stop Stops Clock" toggles control whether the realtime Start and Stop buttons control the clock. Leave them checked, probably. Depending on your sequencer you might actually want to send it a Start message well before it starts receiving clock pulses. The toggles allow you to send realtime messages separately from the clock, or cue them together.
### What about hardware MIDI controls for my sequencer clock, without clicking the buttons with the mouse?
1. Send a bang to a button that has it's Send Symbol mapped to the corresponding symbol for the patch.
2. Check the linked nudgeMidiControls mapping patch in the parent for a tutorial, or the parent_for_link2clockNudge-DNSC2000Map.pd example file includes a stripped down mapping for the Denon DN-SC2000 controller.
