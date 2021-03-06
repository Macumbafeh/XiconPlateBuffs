# XiconPlateBuffs TBC Addon

### [v1.6.1-Beta Download Here](https://github.com/XiconQoo/XiconPlateBuffs/releases/download/v1.6.1-Beta/XiconPlateBuffs_v1.6.1-Beta.zip)

#### Recommended addons to use with XiconPlateBuffs

#### - [BuffLib](https://github.com/Schaka/BuffLib/releases/download/v1.1.1/BuffLib.zip)

XiconPlateBuffs's goal is to accurately show CC in Arena/BG on any nameplate, without the need to hover/target/interact with the nameplate or the nameplate even beeing visible when CC was applied.

This is inferior to PlateBuffer in PvE. PvE is not the main aim for this addon.

## Screenshot

![Screenshot](../readme-media/sample.png)

### Changes

v1.6.1-Beta (hotfix)
- fix font beeing overwritted by nil
- fix testmode

v1.6-Beta
- fix sync errors
- less sync messages (boiled down to aura_apply, aura_refresh, aura_remove, unit_died)
- fix icons appearing twice
- attach unused icons in framePool to UIParent and make the invisible

v1.5-Beta
- SoHighPlates revert to nameplate.oldname:GetText() (more reliant)
- add framePool array to reuse icon frames (less memory usage)
- improve hideIcons (icon's OnUpdate on elapsed timer will recycle itself to framePool)
- shown icons will be reused and timer will be updated (no new icons for active spells)
- add option to edit cooldown font (standard blizz fonts)
- add synchronization between players (also syncs data from CCTracker)
- handle spells from synchronization by spellID to overcome localization
- cooldown text color updated properly
- SPELL_AURA_REMOVED handled separately (sometimes destFlag and srcFlag are different)

v1.4-Beta
- again cleaner hide icons
- cache guid's of known plates
- add debuff handling by guid

v1.3-Beta
- fix register UNIT_DIED event to clear icons

v1.2-Beta
- add support with updated Icicle (https://github.com/XiconQoo/Icicle)
- fix icons reappearing
- cleaner script hooks for OnHide

v1.1-Beta
- add SoHighPlates support
- fix icons not rearranging
- add interface configuration in blizz addons menu (type /xpb or /xpbconfig in chat)
    - size
    - fontsize
    - alpha
    - positioning (x-y offsets)
    - responsiveness toggle
    - sorting
    - test mode
    - default options button


v1.0-Beta

- first dummy working showing CC on nameplates

### TODO

- edit debuff list in config
- add categories
- add icon sizing by debuff/category
- add non cc debuffs
- add important buffs like bubble, innervate etc
- reuse icon frames on nameplates for less memory usage