# Music-Lasers
A Godot 3.2.1 drum machine project

Godot 3.2.1 does not have a way to cache load an audio file and then play it at a specific time, so every time a sample is played there
is a delay, and that delay is inconsistent, causing the audio files to play slightly off beat.

Much of this code can probably be refactored. One step towards this is already done in that every time the user clicks all nodes under
their parent nodes (i.e. all nodes under KickNodes, HatNodes, and SnareNodes) are deleted, and then the grid[x][y] is referenced to
repopulate them. This is followed by the func laser_refresh() which does the same for all the laser sprites, and verifies if a drum
node is in it's path to activate it or not.
