# homebrewRol

Homebrew TTRPG content: one folder per campaign/adventure, with art, maps, PDFs and Homebrewery sources.

## Structure

```
homebrewRol/
├── campaigns/
│   ├── _template/          # Copy this to start a new campaign
│   └── dumrakhal-silk-infestation/        # One folder per campaign
│       ├── README.md       # Synopsis, level range, status, credits
│       ├── art/
│       │   ├── covers/     # Cover-*, Backcover-*
│       │   ├── items/      # Item-*
│       │   ├── locations/  # Location-*
│       │   ├── logos/      # Logo-*
│       │   ├── monsters/   # Monster-*
│       │   └── npcs/       # NPC-*
│       ├── maps/
│       │   ├── battle/     # Encounter / battle maps
│       │   └── world/      # Regional / overview maps
│       ├── documents/      # Exported PDFs, handouts
│       ├── homebrewery/    # Homebrewery markdown source (.md)
│       └── notes/          # DM notes, session prep
└── shared/                 # Assets reused across campaigns
    ├── art/
    ├── maps/
    ├── documents/
    └── homebrewery/snippets/
```

## Adding a new campaign

```sh
cp -R campaigns/_template campaigns/<campaign-name>
```

Then fill in `campaigns/<campaign-name>/README.md`.

## Naming conventions

- Campaign folders: lowercase, hyphen-separated (e.g. `dumrakhal-silk-infestation`).
- Art files keep a type prefix: `Cover-`, `Location-`, `NPC-`, `Monster-`, `Item-`, `Logo-`.
- PDFs: `<Campaign>-<version>.pdf` (e.g. `Dumrakhal-v1.pdf`).
- Homebrewery: paste the brew's markdown into `homebrewery/<name>.md` so the source is versioned, not just the PDF.

## Large files

Images and PDFs make the repo grow quickly. If it gets big, consider [Git LFS](https://git-lfs.com):

```sh
git lfs install
git lfs track "*.png" "*.jpg" "*.jpeg" "*.webp" "*.pdf"
git add .gitattributes
```
