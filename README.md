# 🔫 QBCore Arms Dealer System (Crafting + XP + Smuggling)

Ett komplett och avancerat armsdealer-system för FiveM/QBCore. Systemet kombinerar crafting, rank- och XP-system, smugglingheists med flera faser, vapenproduktion och belöningar – allt paketerat med en stilren HTML5-baserad meny och NUI-effekter.

---

## ✨ Funktioner

### 📈 XP & Rank System
- XP lagras som metadata (`armsdealer_xp`)
- Rank-namn och thresholds definieras i `config.lua`
- Dynamisk rank-up popup via NUI
- XP-belöningar vid crafting, dödade NPC:er och lyckade smuggeluppdrag

### 🛠 Crafting System
- Vapen och ammunition baserat på rank
- Krav på material (metalscrap, copper, steel, osv.)
- Tillverkning sker via NUI-meny med animation, ljud och progressbar
- Zonlåsning möjlig via `Config.UseCraftingZone`

### 🔫 Smuggling Heist System
- 5-fasigt heistflöde med:
  1. Bil + vakter (nycklar krävs)
  2. Lagerstrid + rädda gisslan
  3. Armory där NPC får SMG och väst
  4. Lagerstrid + hämta vapenlåda
  5. Leverera med gaffeltruck
- NPC följer med i/ur bilen
- XP-belöningar vid NPC-kills
- CSS-baserade prompts och notiser (ej QBCore Notify)

### 🎮 UI & NUI
- Responsiv HTML/CSS meny (`html/index.html`)
- XP-bar, rankdisplay, craftingpanel, popup-meddelanden
- Ljud: loot och svetsljud
- Rank-up-popup med upplåsta recept

---

## 🧩 Struktur

```plaintext
qb-armsdealer/
│
├── client/
│   ├── main.lua
│   ├── crafting.lua
│   ├── expsystem.lua
│   └── smuggling.lua
│
├── server/
│   ├── main.lua
│   ├── crafting.lua
│   ├── expsystem.lua
│   └── smuggling.lua
│
├── shared/
│   └── rankutils.lua (valfritt)
│
├── config.lua
├── fxmanifest.lua
│
└── html/
    ├── index.html
    ├── styles.css
    ├── script.js
    ├── loot.mp3
    ├── svets.mp3
    └── img/
        ├── metalscrap.png
        ├── steel.png
        ├── copper.png
        └── ...



OBS KRÄVER ATT DU LÄGGER IN JOBS FILEN I QB-CORE/Shared mappen!! Koden är inte helt buggfri smuggel delen krävs det fortfarande jobb med!
