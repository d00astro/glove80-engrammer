# "Inglorious Engrammer" keymap for MoErgo Glove80

Engram-based Keyboard layout for [MoErgo's Glove80][1].
I call it the "Inglourious Engrrammer", because it is basically just a slightly modified, and for most people likely inferior, version of [Suraj N. Kurapati's (a.k.a Sunaku) "Glourious Engrammer"][2] brilliant keymap for the same device.

Sunaku's layout is an incredibly well thought-through version of [Arno’s Engram][3] layout, with [Miryoku][4]-style layers and [home row mods][5].

### Modifications

My highly personal modifications include:

- Use of fewer keys, so that it could be lift-and-shift'ed over to smaller form-factor and more travel friendly keyboards such as ZSA Voyager.
- Avoid keys that I find uncomfortable. Most notably all the keys in the corners of each hand cluster.
- Number and Symbol layers switched sides. I need the number pad to be operated with my left hand, since in my job I need to operate the mouse while typing numbers.
- Remove layers that I don't use: Dvorak, Colemak, QWERTY, etc
- Combined "World" and Emoji layer.
- Changed the default and and modifiers for "world" characters, most notably putting "diaeresis" (Ä, Ë, Ï, Ö, Ü and Ÿ) as default in order to simplify typing Swedish characters (Å, Ä and Ö)

> ![Photograph of my Glove80 with Engrammer layout](https://raw.githubusercontent.com/sunaku/sunaku.github.io/master/moergo-glove80-keyboard-photograph.jpg)

[1]: https://www.moergo.com/
[2]: https://sunaku.github.io/moergo-glove80-keyboard.html
[3]: https://engram.dev/
[4]: https://github.com/manna-harbour/miryoku
[5]: https://precondition.github.io/home-row-mods

## Keymaps

Sunaku's original:
https://my.glove80.com/#/layout/user/11c0c992-aa4c-4668-9603-456e4558af24

## Installing

Open the [keymap link above](#keymaps) and follow these instructions:

1. Log in (account is required)
2. Clone the keymap to customize and/or build it!
3. Choose your base layout (place at top as layer number #0) via drag & drop.
4. Customize the keymap behavior in this text box.
5. Build the firmware and download the `*.uf2` file.

### Flashing

- For the initial flash, follow "Loading new ZMK firmware onto your Glove80"
  (see page 28 of the [Glove80 User Guide]) or, if that doesn't work, try the
  "bootloader mass storage device mode" method (see page 31 in the user guide).

- If you're installing a different firmware version compared to what your
  keyboard currently has, then ⚠️ **after flashing both halves** ⚠️ perform a
  "Configuration Factory Reset" on both halves (see page 41 in the [Glove80 User
  Guide]) and then turn RGB effects on, watch them illuminate, and finally turn
  them back off. This allows the newly installed firmware to take full effect.

[Glove80 User Guide]: https://www.moergo.com/files/glove80-user-guide.pdf

## Upgrading

- Copy the ZMK snippet from the "Custom Defined Behaviors" text box in either
  keymap linked above and paste into yours. The contents of that text box are
  also available in the `*.dtsi` files provided in this Git repository.

- You can diff and copy changes between a JSON export of your keymap (via
  "Advanced Settings" > "Enable local config" then go back to "Edit" and click
  "Download") and the `*.json` files provided in this Git repository.

## Customizing

You can customize the preset characters in the Emoji and World layers by
editing their respective YAML source files in this repository. Afterwards,
run the `rake` command to regenerate the "Custom Defined Behaviors" snippet.

To install the prerequisite software for `rake` on a Debian GNU/Linux system:

    apt install ruby rake

### Fine-tuning the timing

Activate the typing layer, launch the [QMK Configurator's testing tool](https://config.qmk.fm/#/test), and then pretend to use home row mods. Note the
timing and duration of keystrokes reported by the tool and then use them to
adjust the `#define` time thresholds in the "Custom Defined Behaviors" snippet.

## License

This is a modification of prior art by Suraj N. Kurapati.

Copyright 2023 Suraj N. Kurapati <https://github.com/sunaku>

Permission to use, copy, modify, and/or distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
