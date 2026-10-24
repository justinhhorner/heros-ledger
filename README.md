# Hero's Ledger

A Zelda-styled 100% completion tracker for the N64 version of *The Legend of Zelda: Ocarina of Time*. It is a single static page with no build step and no dependencies.

## What's in it

| Tab | Contents |
| --- | --- |
| Overview | Progress per section, the next step on the story route, and N64 warnings |
| Quest Route | The story in nine phases (52 steps), each with an expandable walkthrough covering dungeon routes and boss fights |
| Heart Pieces | All 36, with how to get each one |
| Gold Skulltulas | All 100, grouped by area, tagged child, adult or night |
| Gear & Upgrades | Items, equipment, capacity upgrades, spells, Medallions |
| Songs | The 12 fixed songs plus the Scarecrow's Song |
| Side Quests | Bottles, Great Fairies, the mask and Biggoron trades, Magic Bean plants, named minigames |

The header shows overall progress, a live heart counter (out of 20) and a Skulltula counter.

## Run it

Open `index.html` in a browser. That's all.

To host it on GitHub Pages: push the repo, then go to **Settings → Pages**, choose **Deploy from a branch**, pick `main` and the `/ (root)` folder, and save. The site appears at `https://<your-username>.github.io/<repo-name>/`.

The page loads two fonts from Google Fonts (Cinzel and Alegreya Sans). Offline, it falls back to system serif and sans-serif fonts and everything else still works.

## How progress is saved

Checkmarks are stored in your browser's `localStorage` under the key `heros-ledger-v1`. They persist across reloads on the same browser and device, and they do not sync between devices. Clearing site data erases them. There is a **Reset all progress** button at the bottom of the Overview tab.

## Editing the content

Everything lives in `index.html`, inside the `<script>` near the bottom:

- `SECTIONS` holds every checklist item as `[id, title, detail, tags]`. Tags are `child`, `adult`, `night` and `hc` (dungeon Heart Container).
- `WALK` holds the walkthrough steps for each Quest Route item, keyed by item id (`r01` to `r52`). Lines starting with `Boss:`, `Mini-boss:`, `Tip:`, `Watch out:` or `Reward:` get a label.

Item ids are what the saved progress is keyed on, so don't renumber existing items. Add new ones with new ids.

## Sources

The checklist was compiled and paraphrased from public guides. Locations are short hints, so open a full guide when one stumps you.

- [Zelda Dungeon](https://www.zeldadungeon.net/wiki/Ocarina_of_Time_Heart_Pieces): Heart Pieces and chapter walkthroughs
- [FinalBoss](https://finalboss.io/the-legend-of-zelda-ocarina-of-time-how-to-get-all-100-gold-skulltulas-n64): Gold Skulltula locations (N64 layouts)
- [Console Pulse](https://consolepulse.com/nintendo/zelda/guides/zelda-ocarina-of-time-complete-guide-100-percent): 100% route, gear and trade sequences
- [GameWith](https://gamewith.net/zelda-ocarina-of-time/76406): dungeon and boss walkthroughs
- [Jegged](https://jegged.com/Games/Legend-of-Zelda-Ocarina-of-Time/Walkthrough): Death Mountain and Goron City steps

It covers the original N64 quest. Master Quest and the 3DS version have different dungeon layouts, so the room-by-room details won't match them.

## Disclaimer

This is an unofficial fan project and is not affiliated with or endorsed by Nintendo. *The Legend of Zelda* and *Ocarina of Time* are trademarks of Nintendo.
