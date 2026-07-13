# Botanical Cask Quest - Gameplay Fact Card

## Core Screen
A vertical craft distillation workshop scene. Top: level title, brief, timer, and stats (temperature, proof, bottles, mistakes). Center: boiler (copper), column, flame indicator, thermometer, three collection jars (heads/hearts/tails), barrel, and bottle. Bottom: action buttons (Fire Low, Fire High, Fire Off, Cut Heads, Cut Hearts, Cut Tails, Dilute, Bottle, Age, Botanical). A recipe panel with material and process step buttons overlays the top half during briefing.

## Core Action
1. Select the correct raw material (e.g. grain, grape, molasses, juniper berry) for the spirit type.
2. Select the correct process steps in order (e.g. Ferment -> Distill -> Botanicals -> Age -> Bottle).
3. Use Fire Low / Fire High to heat the still to the correct temperature.
4. Cut Heads, Hearts, and Tails at the right time based on temperature and proof.
5. Age in the correct cask type, dilute to target proof, and bottle.

## Goal
Produce the target number of bottles at the correct alcohol percentage within the shift duration and mistake limit. Correct material + process flow = Spirit Success. Too many mistakes = Spirit Failed.

## Scoring
- Pass/Fail per level.
- Mistakes tracked against maxAllowedMistakes per level.
- Stars stored locally per level (JSKeyLevelStars).
- Level progression stored locally (JSKeyLevelProgress).

## Progression
50 levels across 5 historic distillery regions, sequential unlock:

| Region | Levels | Spirit | Examples |
|--------|--------|--------|----------|
| London | 1-10 | Gin | First Gin, London Dry, Old Tom, Plymouth, Botanical Mix, Citrus Peel, Sloe Recipe, Hendrick's Style, Monkey 47, London Final |
| Ireland | 11-20 | Whiskey | First Mash, Single Malt, Pot Still Peated, Triple Distill, Sherry Cask, 10 Year, Cask Strength, Blended, Distillery Reserve, Ireland Final |
| Cognac | 21-30 | Brandy | Ugni Blanc, VS Brandy, VSOP Reserve, XO Blend, New Oak Aging, Borderies, Grande Champagne, 20 Year XO, Vintage, Cognac Final |
| Poland | 31-40 | Vodka | Pure Spirit, Triple Distilled, Gold Filtered, Premium Rye, Wheat Vodka, Chill Filtered, Bottle Strength, Flavored, Estate, Poland Final |
| Barbados | 41-50 | Rum | Molasses Wash, White Rum, Aged 3 Years, Dark Rum, Spiced Rum, Cask Strength, Single Cask, 15 Year Reserve, Naval Tradition, Barbados Final |

## Tutorial
Levels 1-3 are guided training:
- L1: Heat the still to 78C.
- L2: Cut Heads at the correct stage.
- L3: Collect 25 mL of Hearts and cut them.

## Instruments
- Boiler temperature: 0-120C
- Condenser temperature: 5-25C
- Current proof: % alcohol
- Heads/Hearts/Tails volume tracking in mL

## Still Types
Pot Still, Column Still, Continuous Still, Vacuum Still

## Cask Types
Bourbon, Sherry, New Oak, Wine, Rum

## Weather Effects
Clear, Fog, Heavy Rain, Blizzard, Thunder (affects ambient temperature)

## Persistence
All data stored locally via NSUserDefaults:
- JSKeyLevelProgress: highest unlocked level
- JSKeyLevelStars: per-level star ratings
- JSKeySoundEnabled: sound effects toggle
- JSKeyMusicEnabled: music toggle

## Monetization and Network
- Offline: no network calls
- No ads, no in-app purchases, no accounts, no analytics, no tracking
