# Mauve Color Tokens

Ready-to-use color tokens for three mauve shades: **mauve**, **dusty mauve** and **dark mauve**. Each comes with a HEX base value and an 11-step scale (50–950) built in OKLCH, shipped as CSS custom properties, a design-tokens JSON file and a Tailwind CSS config.

Interactive versions, palettes, contrast checks and color blindness previews are on [mauvecolor.com](https://mauvecolor.com/).

## Base values

| Name | HEX | RGB | HSL | OKLCH | White text | Black text | Source |
|---|---|---|---|---|---|---|---|
| Mauve | `#E0B0FF` | 224, 176, 255 | `hsl(276, 100%, 85%)` | `oklch(82.7% 0.119 311.6)` | 1.78:1 | 11.82:1 | A Dictionary of Color, Maerz and Paul (1930) |
| Dusty mauve | `#C0AFC5` | 192, 175, 197 | `hsl(286, 16%, 73%)` | `oklch(77.5% 0.036 318.5)` | 2.06:1 | 10.18:1 | Common value in online color-name lists (Color-Name.com, SchemeColor) |
| Dark mauve | `#874C62` | 135, 76, 98 | `hsl(338, 28%, 41%)` | `oklch(49.3% 0.084 356.8)` | 6.48:1 | 3.24:1 | xkcd color survey (2010, CC0) |

Mauve has no single official value. The word is used both for a pale purple (the older dictionary meaning) and for a muted rose. These files use the values above and list where each one comes from. If the exact shade matters, send the HEX value along with the name.

## Scales (50–950)

Each step keeps the base color's OKLCH hue and uses a fixed lightness. Chroma is lowered only where a step would fall outside sRGB. The base color sits at the step closest to its own lightness (shown in bold).

| Step | Mauve | Dusty mauve | Dark mauve |
|---|---|---|---|
| 50 | `#FAF4FF` | `#FCF3FF` | `#FFF3F7` |
| 100 | `#F4E4FF` | `#F6E4FB` | `#FFE3EB` |
| 200 | `#EACBFF` | `#E4D2E9` | `#FFC7DA` |
| 300 | **`#E0B0FF`** | **`#C0AFC5`** | `#EEABC2` |
| 400 | `#BF90DD` | `#B09FB5` | `#D290A7` |
| 500 | `#A476C1` | `#96869B` | `#B6768D` |
| 600 | `#8A5DA5` | `#7C6D81` | `#9A5E74` |
| 700 | `#71448B` | `#645568` | **`#874C62`** |
| 800 | `#5A2E72` | `#4D3F52` | `#673046` |
| 900 | `#44175B` | `#382B3C` | `#501A31` |
| 950 | `#2E0043` | `#241728` | `#39051E` |

## Usage

### CSS

```css
@import "mauve.css";

.card   { background: var(--mauve-100); color: var(--mauve-900); }
.button { background: var(--mauve-700); color: #fff; } /* 7.24:1 with white text */
```

`mauve` is not a CSS named color, so `color: mauve` is ignored by browsers. Use the HEX value or one of the custom properties.

### Tailwind CSS (v3)

Merge `tailwind.config.js` into your config, then use classes such as `bg-mauve-300`, `text-dusty-mauve-700` or `border-dark-mauve`.

### Design tokens

`tokens.json` uses the `$value` / `$type` format from the W3C Design Tokens Community Group draft, which tools such as Style Dictionary and Tokens Studio can read.

## Accessibility notes

- Mauve and dusty mauve are light colors. Use dark text on them; white text fails WCAG AA (1.78:1 and 2.06:1).
- For a button with a white label, use step 700 or darker: mauve-700 `#71448B` reaches 7.24:1, dusty-mauve-700 `#645568` 6.91:1.
- Dark mauve `#874C62` carries white text at 6.48:1 (AA, not AAA).
- To people with red-green color blindness, mauve can look like a pale blue. Don't rely on color alone to signal meaning.

## Method

OKLCH values use the Oklab color space (Björn Ottosson, 2020). Contrast ratios use the WCAG 2 relative luminance formula. All values are rounded to 8-bit sRGB.

## License

CC0 1.0. Use the values however you like. A link back to [mauvecolor.com](https://mauvecolor.com/) is appreciated but not required.
