# Oar Load Calculator

A single-page rowing rigging tool for coaches and riggers. Tell it who is rowing and in what boat, and it gives you the starting rig from the USRowing Level 2 Coaches Manual, then lays out how to make the load a little lighter or a little heavier from there. It's built to be pulled up on a phone at the dock with a tape measure in the other hand, but it works just as well on a laptop.

**Live site:** https://griffin-siadak.github.io/oar-load-calculator/

## What you enter

- **Squad:** Men, Women, Junior Men or Junior Women.
- **Crew average weight**, in pounds or kilograms (the other unit is shown underneath).
- **Boat class:** 1x, 2x, 4x, 2-, 4-, 4+ or 8+.
- **Your rig (optional):** the boat's measured spread (or span, for sculling) and the inboard you're running. These start out filled in with the manual's values. If your boat measures differently, enter what you actually have and the tool keeps the same target loads and works out the outboard and oar length to match.
- **Ladder step:** how far apart each rung of the ladder is, in 0.5, 1 or 2 cm of outboard.

## What you get

**The matched table.** The squad and crew average weight pick which row of the manual's rigging table to use. Men averaging 70 kg (154.3 lb) or less use the lightweight men's row and women averaging 57 kg (125.7 lb) or less use the lightweight women's row, following the World Rowing crew-average limits. Everyone else uses the open row for their squad, and juniors use the junior tables, which have no weight split. The page tells you which table it picked and why.

**Recommended settings.** Spread, inboard, outboard, oar length, baseline load and gearing for that boat. Where the manual gives a range, the tool uses the middle of it, and hovering over spread or oar length on a computer shows the manual's full range.

**An oar diagram** drawn to scale, showing where the collar sits and how the inboard and outboard split the total oar length.

**A load ladder.** Four steps heavier and four steps lighter than the baseline, each one a set change in outboard. Every rung shows the new load and two ways to get there:

- **A, change the oar length:** keep the inboard where it is and lengthen or shorten the oar. This is the more correct adjustment, since the inboard stays tied to the spread.
- **B, move the collar:** keep the oar length and shift the collar with clams (about 1 cm each). This is the quick fix on the dock. Any rung that needs more than two clams gets flagged, since that's past what most coaches would want to do with clams alone.

Gearing is shown for both methods so you can see how each one changes the feel of the stroke.

**When to go lighter or heavier.** A short guide from the manual. Go lighter for a strong headwind, a long race (4k or more) or a novice crew that can't yet row the full stroke. Go heavier for a strong tailwind, a short race (under 1,000 m) or strong athletes who are short in the water. It also covers what each problem looks like from the launch.

## Mobile and desktop layouts

The page checks whether the device's main input is touch and how wide the screen is, then picks a layout. Touchscreen laptops count as desktop, since their main input is still a mouse or trackpad. It does not rely on the browser's user agent.

- **Mobile** (phones and tablets: any device whose main input is touch, or any screen 760 px wide or less): the results come right after the crew inputs and the rig adjustments move below them. The ladder shows one method at a time, with a switch between "Oar length" and "Collar (clams)", so the table fits without sideways scrolling. Buttons and inputs are sized for thumbs, the number fields bring up a decimal keypad, and the oar diagram is redrawn so its labels stay readable.
- **Desktop:** inputs on the left, results on the right, and the full ladder with both methods side by side.

If the page guesses wrong, a switch at the bottom forces the other layout. The browser remembers that choice until you set it back to automatic.

## How the numbers work

From the manual, Module 5, Chapter 2:

- Load (sweep) = outboard ÷ spread
- Load (sculling) = outboard ÷ (span ÷ 2)
- Gearing = outboard ÷ inboard
- Outboard = oar length − inboard

Rules of thumb the page also lists: sweep inboard is about spread + 30 cm (±1), and sculling inboard is about (span + 18 cm overlap) ÷ 2.

The manual doesn't scale load by body weight within a table, so this tool doesn't either. Crew weight only decides between the lightweight and open tables. Use the ladder to fit your crew's size and strength.

## Limits

The baseline comes from the manual's club-level table, and every number here is a starting point rather than an answer. Measure your own rig, row, race and watch the boat, then adjust. For newer blade shapes such as fat blades, the blade maker's recommendations should come first.

## Running it

Open `index.html` in any browser, or use the live site. There's no build step and nothing to install; everything is in that one file. GitHub Pages publishes straight from the `main` branch, so whatever is pushed to `main` goes live within a minute or two.

## Source and disclaimer

The rigging figures and formulas come from the USRowing Level 2 Coaches Manual (Module 5, Chapter 2 and the Figure 7 club-level rigging table). Lightweight cutoffs use World Rowing crew-average limits. This is an independent tool, not affiliated with or endorsed by USRowing.

Suggestions or corrections are welcome: email siadak.griffin@gmail.com or open an issue on this repo.

## License

Apache License 2.0. See [LICENSE](LICENSE).
