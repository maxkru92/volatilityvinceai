# KC Krupp Capital — Volatility Vince AI

Vercel-deployed scaffold for **volatilityvinceai.vercel.app**, branded with the KC **cyan** favicon variant from the [Krupp Capital favicon pack](/Users/maximiliankrupp/Desktop/kc-favicon-pack).

| constant        | value   |
|-----------------|---------|
| Pine Script     | `C_CYAN` |
| c1 (canonical)  | `#00E5FF` |
| c2 (deeper)     | `#00B8D4` |
| persona         | Volatility Vince AI |

## Local dev

```bash
npx serve public -l 3000   # http://localhost:3000
```

## Rebuild favicons

```bash
npm run kc:deploy   # runs deploy.py --sites=volatilityvinceai (idempotent)
```

## What lands in `public/`

| file                         | purpose                              |
|------------------------------|--------------------------------------|
| `favicon.ico`                | legacy windows shortcut              |
| `favicon.svg`, `icon.svg`    | modern gradient                      |
| `favicon-16.png`             | browser tab @1x                      |
| `favicon-32.png`             | browser tab @2x                      |
| `apple-touch-icon.png`       | 180×180 iOS home screen              |
| `icon-192.png`, `icon-512.png` | PWA icons                          |
| `og-image.png`               | 1200×630 social share                |
| `site.webmanifest`           | PWA manifest, theme_color = {P['c2']} |

## Deploy to Vercel

```bash
vercel link --yes
vercel deploy --prod
```

Vercel auto-detects static-site mode and serves `public/` from the URL root.


> **Note:** `package.json` no longer carries the `kc:deploy` script (removed to keep it portable across machines). The deploy recipe is documented above in **Regenerate favicons**.
