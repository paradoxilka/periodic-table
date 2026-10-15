# periodic table

I wanted a periodic table I could actually poke at — click an element and see its
shells, its spectrum, what it reacts with, and how much heat comes out. Everything I
found was either a static image or a wall of text, so I built my own.

It's one HTML file. No build step, no dependencies, no npm install. Open it and it works.

Live version: https://paradoxilka.github.io/periodic-table/

<img width="1919" height="812" alt="image" src="https://github.com/user-attachments/assets/fb7ee653-f042-4be2-8c2f-62814a3e784b" />


## What you get

Click any element and a panel opens with six tabs:

- **overview** — the usual suspects: mass, density, melt/boil, electronegativity, IE1, E°, radius, discovery info
- **molecule** — what form the element actually takes at room temp (H2, S8 crown, graphite layers, metallic lattice...) with a little drawing of it, plus the energy needed to rip it into free atoms
- **shells** — animated Bohr model, electrons orbiting per shell
- **spectrum** — emission lines plotted by wavelength, colored correctly, hover a line to read it
- **isotopes** — stable vs radioactive, abundances, half-lives, and the proper names where they have them (protium, deuterium, tritium, thoron...)
- **reactions** — every element it reacts with, with a balanced equation, the ΔH, and whether it's exo or endothermic

The fun bit is the **reaction lab** up top: turn it on, click any two elements, and it
tries to write the reaction between them. If I have real thermochemistry for the pair, you
get the actual numbers. If not, it estimates the product from oxidation states and says so
(marked `EST`). If they genuinely don't react — noble gases, two metals that just alloy —
it tells you that instead of making something up.

Other stuff:
- "reacts with" toggle highlights everyone a given element reacts with on the grid
- compare mode puts up to 4 elements side by side on any property
- heatmap recolors the whole table by one property (try density or ionization energy)
- search + family filters

## honest caveats

The data is from standard CRC/NIST-type references as I know them, which is good enough
for learning and intuition but I wouldn't bet a synthesis on it. ΔH values are per reaction
as written at 298 K. Anything marked EST is a guess from oxidation states — deliberately
no fake numbers. For real work, check NIST.

Also, the spectra are representative lines, not full arc spectra (those have hundreds of lines).
