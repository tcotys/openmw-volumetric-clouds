# Zesterer's Volumetric Cloud & Mist Mod for [OpenMW](https://openmw.org/en/)

A mod that adds raycasted volumetric clouds to Morrowind.

The goal of this mod, aside from looking pretty, is to enhance the perception of the world's scale. High view
distances are great, but they ruin the sense of immersion and mystery. Equally, a low, static view distance has the
opposite problem: you never get the opportunity to see the sights. With this mod, you'll experience the best of both
worlds: mystery and intrigue, with occasional moments of wonder when the mist clears and you can see for miles.

[![A view over Vivec, looking north-east](https://i.imgur.com/UH4TMey.png)](https://www.youtube.com/watch?v=60jWROy5Pdg)
[![Mist outside Vivec](https://i.imgur.com/eUuck8r.png)](https://www.youtube.com/watch?v=60jWROy5Pdg)
[![Volumetric clouds in the distance over Red Mountain](https://i.imgur.com/SaoByZR.png)](https://www.youtube.com/watch?v=60jWROy5Pdg)
[![Dawn in Vivec](https://i.imgur.com/C7Sm02j.png)](https://www.youtube.com/watch?v=60jWROy5Pdg)
[![A misty night in Seyda Neen](https://i.imgur.com/c2NTbez.png)](https://www.youtube.com/watch?v=60jWROy5Pdg)

## Installing the mod

Note: This mod requires the (soon to be merged) [OpenMW Post-Processing patch](https://gitlab.com/OpenMW/openmw/-/merge_requests/1124).

As with most mods, place the files into their own directory and point your `settings.cfg` at it.

*TODO: More detailed instructions*

## Enabling the mod

- Press F2 to open the in-game post-processing menu

- Click on 'clouds'

- Press the right arrow key to add it to the active effects list

## Configuration

The mod comes with a variety of configuration options. You can:

- Change render quality (lower quality means higher performance)

- Alter cloud density

- Alter mist density

- Toggle an additional 'swirling' effect that makes mist more realistic and interesting to watch

- Toggle clouds on and off

- Toggle whether the vanilla skybox is visible behind the clouds and mist

## Performance

Performance may be an issue for some machines. The mod includes a variety of settings (available in the aforementioned
F2 menu) that allow reducing the quality or disabling various features in order to improve performance. At minimum
settings, even the lowest-powered machines *should* be able to run the mod.

## Implementation

- Both clouds and mist are rendered using raycasting, meaning that they are 3D elements of the environment: you can
  walk through them and they swirl, shift, and move in real time.

- Although all code is new to the mod, many aspects of the implementation are borrowed from my work on
  [Veloren](https://veloren.net/)'s cloud shaders.

## Known issues

- Rain is applied before post-processing shaders and don't write to the depth buffer, so clouds appear over rain drops
