# ISKRIT rebar cutting guide

[Open the free rebar cutting calculator](https://iskrit.pro/en/instrument/raskroy/) · [ISKRIT engineering tools](https://iskrit.pro/) · [Русская версия](https://iskrit.pro/ru/)

ISKRIT is a browser-based tool for one-dimensional rebar cutting optimization. Enter required cut lengths and quantities, or import an Excel bar schedule, to prepare cutting patterns and review stock use and remnants. The calculator is free to use without registration.

This repository contains a practical introduction and a small example dataset. It documents the hosted calculator; it does not contain its source code.

## What the calculator supports

- Multiple stock lengths, saw kerf and reusable offcuts.
- Excel bar schedule import.
- Cutting maps exported to XLSX or printed for workshop use.
- Cut-length calculation from dimensions for supported BS 8666 shape codes.
- English and Russian interfaces.

It can help construction engineers, rebar fabricators and small workshops plan cuts in linear stock.

## Prepare the input

1. Separate bars by diameter, grade and any other requirement that prevents them from being interchangeable.
2. Enter the required **cut length** and quantity for each group. A bent bar's cut length can differ from its overall dimensions.
3. Enter available stock lengths and any reusable remnants.
4. Set the saw kerf in the same unit as the lengths.
5. Review the proposed patterns, stock requirements and remaining lengths, then export or print the cutting map.

The example below uses millimetres. Check the selected unit in the calculator before entering it.

## Worked example: straight bars from 12 m stock

Assume one interchangeable bar group, unlimited 12,000 mm stock, and a 5 mm allowance for each cut. Required pieces:

| Cut length (mm) | Quantity |
| --- | --- |
| 4,200 | 6 |
| 3,100 | 8 |
| 1,800 | 10 |

The total finished length is **68,000 mm**. One feasible arrangement is:

| Stock bars | Pattern | Pieces per bar | Kerf per bar (mm) | Remainder per bar (mm) |
| --- | --- | --- | --- | --- |
| 3 | 4,200 + 4,200 + 3,100 | 3 | 15 | 485 |
| 1 | 3,100 + 3,100 + 3,100 + 1,800 | 4 | 20 | 880 |
| 1 | 3,100 + 3,100 + 1,800 + 1,800 + 1,800 | 5 | 25 | 375 |
| 1 | 1,800 × 6 | 6 | 30 | 1,170 |

This uses six stock bars: **72,000 mm = 68,000 mm finished pieces + 120 mm kerf + 3,880 mm remnants**. At least six 12 m bars are needed because the finished length alone exceeds five bars. This is an illustrative hand-checked arrangement, not a claimed output from a particular calculator run. Other arrangements can distribute the remnants differently.

The [example CSV](example-cut-list.csv) contains these lengths and quantities. Open it in a spreadsheet and use it as a reference when preparing an Excel bar schedule; it is not a claim that CSV is an accepted import format.

## Interpret the result

Stock count, total leftover length and the usefulness of individual remnants are different measures. A long remnant may be worth saving, while several short remnants may not be. Include actual stock availability, kerf, usable remnant lengths and any workshop allowances when comparing plans.

The cutting plan organizes material use. Check the bar schedule and fabrication requirements before production.

## Try the tool

[ISKRIT Rebar Cutting Calculator — free, no registration](https://iskrit.pro/en/instrument/raskroy/)

The wider [ISKRIT toolkit](https://iskrit.pro/) includes engineering calculators for construction, surveying and laboratory workflows.

