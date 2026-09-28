# myles.calculator

A modern multi-mode calculator for the Omarchy bar: scientific, programmer, currency, units, tip/VAT, and history.

A modern multi-mode calculator for the Omarchy bar: scientific, programmer, currency, units,
tip/VAT, and history.

## What it does

| Mode | What you get |
| --- | --- |
| Basic | Arithmetic with keyboard and button input, running history |
| Scientific | Trigonometry, logs, powers, constants, unit suffixes |
| Programmer | Bitwise ops, base conversion (2/8/10/16), and byte/bit views |
| Currency | Live FX conversion between currencies |
| Units | Length, mass, area, volume, speed, temperature, data, and more |
| Tip & VAT | Split a bill, apply tip and tax, divide the total |

Invoke it from the bar, or type `calc`/`fx`/`convert` in the Omarchy launcher.

## Network calls

**Currency mode fetches live rates from `https://open.er-api.com/v6/latest/`.** This is the
only network access in the plugin; all other modes are fully offline. If you are offline,
currency mode falls back to the last cached rate set.

## Requirements

None. The engine and converters are plain JavaScript, evaluated in-process.

## Install

```bash
omarchy plugin add https://github.com/Omarchy-plugin/myles-calculator.git --enable --yes
```

That clones, validates, installs to `~/.config/omarchy/plugins/myles.calculator/`, and places it on your bar.

## Update

```bash
omarchy plugin update myles.calculator --yes
```

Or update every git-managed plugin at once:

```bash
omarchy plugin update --yes
```

## Uninstall

omarchy plugin remove myles.calculator --yes

## Credits

- Built for [Omarchy](https://omarchy.org).
- Mylesoft — <https://github.com/Omarchy-plugin> — modifications.

Plugins run unsandboxed inside the long-lived `omarchy-shell` process with your user
permissions. Review the source before enabling anything you did not write.
