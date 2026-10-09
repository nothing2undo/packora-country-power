# Plugs, sockets and mains voltage by country

A table of the plug types, socket voltages and supply frequencies of 243 countries and
territories, keyed by ISO 3166 country code. It is the table the Packora packing-list app uses to
tell whether a traveler needs a plug adapter.

## The file

`country_power.csv`, one row per country or territory:

| Column | Meaning |
|---|---|
| `code` | ISO 3166-1 alpha-2 code (plus `IC`, `EA`, `XK` and similar codes in common use) |
| `country` | English name |
| `main_plugs` | Plug types in everyday use there, space-separated letters A to O: what a traveler from there has on their devices |
| `all_plugs` | Every plug type listed for the place, including ones only found in older buildings or some regions: what a visitor may find in the wall |
| `voltages` | Nominal single-phase voltages at sockets, space-separated where there is more than one |
| `frequencies` | Supply frequencies in hertz |
| `sources` | Which source the row rests on, see below |

Plug letters are the ones the IEC uses in its "World Plugs" list.

## Sources and credits

This table is derived from two sources.

- **Wikipedia, "Mains electricity by country"**, by Wikipedia contributors.
  https://en.wikipedia.org/wiki/Mains_electricity_by_country
  Licensed [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
  Retrieved 2026-10-06 (voltages, frequencies) and 2026-10-09 (plug types).
- **PlugVoltage power-compatibility dataset**, version 2026.09.30.2 (2026-09-30).
  https://plugvoltage.com/data/power.json
  Licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
  Its own per-claim sources are listed in the dataset.

What the `sources` column says:

| Value | Meaning |
|---|---|
| `wikipedia` | Both plug columns are what Wikipedia lists |
| `wikipedia + plugvoltage` | One of PlugVoltage's 40 countries: `main_plugs` is PlugVoltage's socket types, `all_plugs` is what either source lists |
| `same as XX` | A territory Wikipedia does not list, given the values of the country it belongs to |

Changes made to the sources: reduced to plug types, voltages and frequencies; names replaced by
country codes; the two sources combined as described above; territories filled in from their
country.

## Licence

The table is licensed under the
[Creative Commons Attribution-ShareAlike 4.0 International licence](https://creativecommons.org/licenses/by-sa/4.0/)
(CC BY-SA 4.0). You may use and adapt it, also commercially, if you give credit as above and
offer what you derive from it under the same licence. The full text is in `LICENSE`.

## No warranty

The table is a compilation of public sources and may contain errors. Check the plug and the
voltage before plugging a device in abroad.
