# Xork I

Play the original **Zork I** on your own Windows PC, with a companion who speaks as you explore and
pictures of each room as you reach it. The companion's lines and the pictures come from AI models that
run on your own graphics card: after installing, nothing goes over the internet, and there's no account
or sign-in.

Your companion is **Sybylla**, in the voice of Sybylla Melvyn, the narrator of Miles Franklin's
*My Brilliant Career* (1901). She's a work in progress.

## What you need

- **Windows 10 or 11** (64-bit).
- **An NVIDIA graphics card** with a current driver ([nvidia.com/drivers](https://www.nvidia.com/drivers)).
  How much memory it has decides which pictures you can have:

  | Room pictures | Graphics memory | Download |
  |---|---|---|
  | Best (FLUX.2 klein, in the game's own picture style) | 16 GB | about 23 GB |
  | Better (SDXL-Turbo) | 12 GB | about 14 GB |
  | Good (SD-Turbo) | 8 GB | about 9 GB |
  | No pictures | 4 GB | about 3.6 GB |

  The installer finds your card and picks the choice that fits. You need a little more free disk space
  than the download.

## Install

1. Download **Play-Xork-I-Setup.exe** from the [latest release](https://github.com/wgruner/xork-i/releases/latest).
2. Run it. The installer isn't signed, so Windows may say **"Windows protected your PC"**: click
   **More info**, then **Run anyway**.
3. Choose your room pictures and confirm the download size. The installer then downloads
   Python, Sybylla's model and the picture model, showing how far it has got. This can take an hour or more on a slow connection.
   If it's interrupted, run the installer again and it carries on where it stopped.

Nothing needs administrator rights; it all goes in your user folder
(`%LOCALAPPDATA%\Programs\Xork I`).

## Play

Open **Play Xork I** from the Start menu. The game opens in your browser, and its icon appears by the clock.
Type commands like `open mailbox`, `go north` or `take lamp`. Sybylla's line and the room's picture
follow a moment after the game's reply. Each time you start, the models take a minute or two to load,
so the first few moves may come without a picture or a line.

**While the game runs, Xork I puts an icon by the clock.** Click it to open the game; right-click it
for more, including **Quit Xork I**. Quit when you've finished: closing the browser leaves the game
running, holding your graphics card's memory. If you can't see the icon, it may be under the **^** arrow
beside the clock.

Your game is saved after every move, so next time you start, it carries on where you left off;
**New game** starts over.

The map beside the picture shows every room you've been through, with north up. It stays at the same
size and follows you as you move; scroll it, or drag it with the mouse, to look around, and click
**Recenter** to come back to where you are. If you installed with no pictures, the opening scene stays in
the picture's place.

## Uninstall

Settings → Apps → **Xork I** → Uninstall. This removes everything it downloaded, and your saved game.

## Credits and licenses

Xork I is a non-commercial fan project. It isn't affiliated with or endorsed by the owners of the
"Zork" trademark.

- **Zork I** (release 119) is from [historicalsource/zork1](https://github.com/historicalsource/zork1),
  under the MIT License, run by the [fernz](https://pypi.org/project/fernz/) interpreter.
- **Sybylla's model** is a fine-tune of NVIDIA Nemotron 3 Nano 4B, licensed by NVIDIA Corporation under
  the [NVIDIA Open Model License](https://www.nvidia.com/en-us/agreements/enterprise-software/nvidia-open-model-license/).
  It runs on [llama.cpp](https://github.com/ggml-org/llama.cpp) (MIT). It and the picture style are on
  Hugging Face at [wgruner/xork-i-assets](https://huggingface.co/wgruner/xork-i-assets).
- **Pictures**: [FLUX.2 klein 4B](https://huggingface.co/black-forest-labs/FLUX.2-klein-4B) (Apache 2.0);
  [SD-Turbo](https://huggingface.co/stabilityai/sd-turbo) and [SDXL-Turbo](https://huggingface.co/stabilityai/sdxl-turbo),
  licensed under the Stability AI Community License, Copyright © Stability AI Ltd. All Rights Reserved.
  Powered by Stability AI.
- The game's own code is under the MIT License; the installed copy includes it, with `LICENSE` and
  `THIRD_PARTY_NOTICES.md`.
