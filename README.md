# levo4-geo

Levo 4 Geo Combos: a geometry calculator for the Specialized Turbo Levo 4 and Levo 4 EVO.

Pick the stock bike, frame size, shock extension (standard Low/High or EVO 230×62.5), Horst pivot chip, upper headset cup, fork travel, axle-to-crown and offset. The page shows head angle, seat angle, reach, stack, BB height and drop, chainstay, wheelbase, front center, trail and travel, each compared against the stock bike.

It's a single static page (`index.html`) with no build step, served by GitHub Pages.

## Where the numbers come from

- **Stock geometry** for the Levo 4 (S1–S6) and Levo 4 EVO (S2–S6) is Specialized's user-manual geometry chart. A setup that matches a stock bike exactly is tagged "Specialized chart."
- **Chip and cup changes** use the manual's adjustment table (section 11.1):

  | Adjustment | Chainstay | BB height | Head angle |
  |---|---|---|---|
  | Horst pivot Long | +11 mm | −12 mm | −0.8° |
  | Headset cup −1° / +1° | — | −2 / +2 mm | −1° / +1° |
  | Shock extension Long (High chip) | −2 mm | +6 mm | +0.4° |

  The EVO extension has no High/Low setting.
- **Everything else is calculated.** Chip and fork changes tip the whole frame, so reach, stack and seat angle rotate with it. A longer fork tilts the frame back about 0.4° per 10 mm of axle-to-crown. Run with the EVO link and a 597 mm fork, the model reproduces Specialized's published EVO chart within 1.3 mm and 0.2°.
- **Forks:** pick a Fox 36 (2023–27, incl. E-Optimized), Fox 38 (2021–26 or 2027), RockShox ZEB, or Custom. Axle-to-crown comes from the makers' spec sheets, and travel is limited to what each fork comes in:

  | Fork (29") | 140 | 150 | 160 | 170 | 180 | 190 |
  |---|---|---|---|---|---|---|
  | Fox 36 (2023–27) | 556.0 | 566.0 | 576.0 | | | |
  | Fox 38 (2021–26) | | 563.7 | 573.7 | 583.7 | 593.7 | |
  | Fox 38 (2027) | | | 578.6 | 588.6 | 598.6 | |
  | RockShox ZEB | | 566 | 576 | 586 | 596 | 606 |

  Specialized's charts use one nominal length (577 mm at 160, 597 mm at 180) for every trim; the stock comparisons use that. Custom takes any A2C and offset.
- **Headset cup and reach:** reach doesn't change. The cup tips the frame slightly, which moves the head tube back about 3 mm on a +1° cup, but the steerer leans about 2 mm forward, so the stem lands within a millimeter of where it was. Stack (+2 mm) and seat angle (−0.25°) do change on a +1° cup and are included.
- Wheelbase and front center for chip and cup changes are estimates; the manual lists chainstay changes but not wheelbase.

All figures are static and unsagged.

## Caveats

- Specialized rates the Levo 4 frame for forks up to 180 mm.
- The EVO extension (part S256300003) needs a 230×62.5 standard-eye shock. A 230×65 isn't supported on it.
- Specialized's marketing lists the long chainstay as 444 mm; the manual's table gives +11 mm. This calculator follows the manual.
