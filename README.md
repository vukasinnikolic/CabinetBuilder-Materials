# Kitchen Planner materials (2K)

The scanned material sets [Kitchen Planner](https://github.com/vukasinnikolic/CabinetBuilder) downloads for
renders, at 2048 px. The app itself ships the same sets at 1024 px (roughness at 512 px).

All of it is CC0 1.0 (see `LICENSE`): scans from [ambientCG](https://ambientcg.com), listed asset by asset in
`SOURCES.md`. Made by `apps/desktop/scripts/scanned-materials.py pack2k` in
[vukasinnikolic/CabinetBuilder](https://github.com/vukasinnikolic/CabinetBuilder).

## Layout

The same paths as the app's `apps/desktop/src/renderer/src/assets/textures/`:

- `wood/<species>.jpg`, `tile/<name>.jpg`, `countertop/<Family>/<Family>NN.jpg` - the colour picture.
- `<name>_n.webp` - normal map, OpenGL convention (+Y up the picture); none on polished granite, quartz and
  marble.
- `<name>_r.webp` - roughness in grey RGB, mean 0.75 (the renderer scales it to the finish's roughness).

## manifest.json

```json
{"version": 1, "size": 2048, "files": {"wood/oak.jpg": {"size": 123456, "sha256": "<hex>"}, ...}}
```

`files` lists every picture and map (paths sorted, forward slashes) with its size in bytes and SHA-256; the
README, LICENSE, SOURCES.md and the manifest itself are not in it.

## Changing it

Never rewrite history or change a file in place: add a new commit. The app pins a commit.
