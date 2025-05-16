# SCAR Character Sheets
The SCAR system is a tabletop roleplaying game currently in active development. You can find the docs [Here](https://scar-srd.com). Because it is in active development, rules and mechanics may change rapidly, even within the course of a day. I am not a part of SCAR's development, so I cannot always update this sheet to be totally abreast of the changes. 

## How to Use this
To make this system more approachable, I created this HTML and CSS to be used in [Roll20](https://roll20.net). To use custom character sheets, you must be a Pro user on
Roll20, which as of writing is 10 USD a month, or 100 USD a year.

To use the custom character sheet:
1. Open your campaign in Roll20, but do not launch it.
2. Navigate to Settings > Game Settings
3. Scroll to the bottom, where it says "Character Sheet Template", and change to Custom.
4. Copy the contents of SCAR.html into the HTML Layout tab.
5. Copy the contents of SCAR.css into the CSS Styling tab.
6. Save your changes!

## Using the Sheet
The sheet is laid out similarly to the official SCAR character sheets, although broken out into separate tabs, as described below. On all tabs, you will be
able to see the blocks containing your player's name, species, and other info.

All dot-dice buttons take all the rules into account. Roll20 doesn't natively support counting a critical success as 2, so all true dot dice rolls must be done through a button, or you will need to resort to manually counting.

### Basic
The basic tab contains the blocks for your general attributes.
- Quick Reference Stats includes your HP, Exhaustion, Evasions, Integritys, Soul Save, and Boosts per session.
- Movement breaks your movement distances out by type. 
- Make Skill Check is a utility button that performs a dot roll for a certain skill check. The system will prompt you for the Attribute, Expertise, and Skill you want to use, as well as the difficulty of the check.
- Do Dot Roll is a utility button that performs any dot roll you wish. The system will prompt you for the pool size, the difficulty, and the explosion threshold.
- Attributes, Expertises, Natural Skills, Trained Skills, and Knowledge Skills are broken out into separate blocks. The B column is for bonuses for each stat.
- There is an additional block at the end for custom skills. Click "Add" and "Modify" to adjust them.

### Combat
The Combat tab contains useful blocks for being in combat.
- Quick Reference Stats and Movement are the same as the Basic table
- The Stat Change block are changes to your battle stats. They are divided in two: In Battle changes end at the end of battle, while Out of Battle changes last long-term, possibly forever.
- The Conditions block are afflicitions you've received during battle. Any number of conditions can be applied at once. The "Clear All" button will remove all conditions you have.
    - Name is the name of the condition. This is free-text, to support custom conditions.
    - Level is the level of the condition. Conditions start at Level 1, and can increase up to Level 3. Each successful Cleanse reduces the level by 1.
    - Save is the threshold you need to hit on a Cleanse attempt for a success. The save is equal to the *inflictor's* Soul + Expertise + Skill, divided by 2, plus any bonuses.
    - The Cleanse button will help you attempt a Cleanse action. If the number rolled is greater than or equal to the save, the level is decreased by 1.

### Attacks
The Attack tab also contains useful blocks for being in combat.
- Combat Attributes lets you reference the attributes you use for moves.
- Combat Skills lets you reference the skills you use for moves.
- EXP Caps describe the amount of EXP and Power you are allowed to use when creating a move of each Action type.
- Utility buttons are provided for generic attacks. You can also use the attack block itself to automatically fill out most of this info.
    - Roll Move Accuracy is a utility button that lets you perform an Accuracy roll for moves. It will prompt you for the Attribute, Skill, STAB, and base Difficulty.
    - Roll Effect Accuracy is a utility button that lets you perform an Accuracy roll for effects. It will prompt you for the Skill and base Difficulty.
    - Roll Power is a utility button that lets you perform a Power roll. It will prompt you for the Attribute, Skill, Base Power, whether it's a Crit, type effectiveness, and base Difficulty.
- You may then add each Attack as a separate block using the "Add" button. Each move block contains:
    - The move name
    - Whether the move is Physical or Special
    - The skill to use in the roll. This should match, case-insensitively, the stat name.
    - The element of the move, such as "Basic"
    - The base accuracy of the move
    - The base power of the move
    - The range, such as Melee
    - The EXP to construct the move. The first number is the total EXP you used, and the second number is the max EXP.
    - The type of action the move is.
    - Roll Accuracy is a utility button. The contents of the block are pulled in automatically, so it just asks if it's STAB and the base difficulty.
    - Roll Power is a utility button. The contents of the block are pulled in automatically, so it just asks if it's a crit, if there is a type advantage, and the base Difficulty.
    - Extra Effects is free text for any notes. I recommend the EXP cost breakdown, and any math you did.

### Feats
The Feats tab contains a list of all the feats you've taken. Click "Add" to add one.
- The feat's name
- The feat's effect. You may put any text in here.

### EXP/Merits
This tab allows you to record all your EXP and Merit purchases. This is essential, in case you need to have anything refunded. EXP is on the left side, and Merit is on the right side. Both have the same fields, as described below:
- The amount of EXP or Merits spent so far. This takes discounts into account.
- The total amount of EXP or merits you've earned.
- The amount of discounts you've received on EXP or Merits.
- The effective amount of EXP or Merits spent. This does *not* take discounts into account.
- Purchase Info is the name of the item you purchased.
- Initial is the base amount of EXP or Merits this item costs.
- Discount is any discount you received purchasing the item.
- Final is the Initial EXP minus the Discount.

### Inventory
This tab allows you to record your inventory. At the top are some useful fields:
- The amount of money you have.
    - Currency names can be customized to fit your setting.
    - Checking "Auto Rollover" will enforce rollover and rollunder rules. This means Copper and Silver amounts will be normalized
    to always be between 0 and 9, distributing higher or lower pieces as necessary. If unchecked, all fields will be totally manual.
        - Rollover rules will assume that 10 of the rightmost currency equals one of the middle currency, and 10 of the middle currency equals 1 of the leftmost currency.
        - Negative Silver or Copper pieces are supported. When Auto Rollover is enabled, this will decrease the next-highest unit by 1, and normalize the unit between 0 and 9. As an example, 5 Gold -1 Silver would become 4 Gold 9 Silver.
- The current bulk of your entire inventory.
- The maximum bulk you can carry.
- A checkbox which indicates if you are encumbered.
- A checkbox which indicates if you are overencumbered.

After clicking Add, you can use these fields:
- The name of the item
- The bulk of the item, in intervals of 0.1.
- The number of that item you have.
- The total, which is equal to the bulk times the quantity.

### Init Character
This button is not a tab, but instead initializes a character. It will:
1. Set total EXP to 100
2. Add a normal type physical attack of Power 4 to the Attack Pool
3. Add four type-related feats to the Feat pool: two Type Affinity, and two STAB Affinity.

Note that this doesn't actually clear anything out, so it is not explictly dangerous to hit it by accident.

## Known Issues
- Damage Rolls always assume you want the 1.5x bonus for a Crit. If you want the option for exploding 9s, you will have to roll manually for now.
- Current Bulk display gets squirrely when using numbers not representable in binary, such as 0.3. 
- Max Bulk could be computed, but currently is manually entered.
- Temp HP and Current HP are separate stats, so displaying hp in a token bar will not show the Temp HP. Extra Max HP *is* factored into Max HP, so that will display correctly.

## Future Enhancements
- Armor section. (Armor is currently being heavily edited, so I won't add this until it's stable)
- Display condensed Attack List on Combat tab
- Typing Block as a Global block