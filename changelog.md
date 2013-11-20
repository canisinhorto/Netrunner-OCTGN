Changelog
---------
### 3.1.1.x

* Fixed some card typos and bad keywords

### 3.1.0.x

* Version made to work with the OCTGN 3.1.x

### 3.0.2

* Made custom fonts work again with new version of OCTGN

### 3.0.1

* The Shell traders should now work at the start of your turn instead of the end

### 3.0.0

We are DONE ladies, gentlepeeps and people in between. Finished! Fertig! Finito! ?????!
Version 3.0.0 marks the end of active development for this plugin by me. There may still be bugfixes and perhaps minor tweaks here and there, but the main functionality is all there.

I'll now be concentrating my efforts into porting this plugin to run Android: Netrunner. Expect the same level of goodness there ;)

So, final changes for this version

 * Memory check now made a function. Will also work for cards installed via shell traders
 * Made findTarget() and per() targeting exclude cards highlighted as Dummies, Revealed, or Inactive
 * Polished and restructued the code a bit. Unfortunately no extensive commenting yet. My future self will probably hate me.
 * Also fixed some bug with the debugverbosity
 * InflictX will not warn you if you're doing 0 damage now.
 * Fixed bug with checking for Noisy cards
 * Added AutoScript for the runner's Counter Hold. Now it is able to select and remove special markers given to him by the Corp.
 * Added custom code for all markers which have effects I can code (eg. Mastiff, Data Raven, Fang, Doppelg�nger, Boardwalk etc)

### 2.1.11

 * Made deck checking faster.
 * Added functions which allow the players to trash other player's cards and also take care of their effects
 * Added function which allows markers on your counter hold to initiate effects of their own at turn start/end.

### 2.1.10

 * At turn start/end effects now trigger more robustly.
 * RequestInt can now be passed a special announcement to use
 * Checking for tags can now be used on other core commands than InflictX
 * Stopped using the old scripts completely
 * Cards which modify your draw


### 2.1.9

 * **Fixed significant bug** with Core set programs & hardware, where they wouldn't activate their "onInstall" autoscrips. Please download patch -v5 to fix
 * Cards revealed randomly from hand now get a special highlight and don't trigger trash effects.
 * Made some tweaks to deck checking which should make it faster
 * Playing a noisy card will now waste money out of your stealth cards according to its rules
 * Added a "Prioritize card" function, which marks a card for using its counters for an automatic effect it applies to, before the others
 * Targeted cards get secondary priority after the priority cards.
 * Added trigger for starting automatic effect at the start of runs (e.g. see Cerberus)
 * Now action # will aut-adjust in case the player modifies their counter or uses an effect to gain or lose some.


### 2.1.8

Proteus now Fully Automated!

Most changes in 2.1.7, so take a look there for an idea of what to expect ;)

### 2.1.7

 * Added function which intercepts and reduces counter increase commands depending on specific markers. 
 * Autoscrip to request and number and re-use it elsewhere.
 * Current action is now displayed via a global variable.
 * TransferX now works for counter "forfeit" effects
 * Made invalid Start-of-Turn check work more robustly.
 * Many other bugfixes
 * Now InflictX can be used as a cost with -isCost. As long as some damage is inflicted, the next part of the Autoscript will work, otherwise it will exit but the cost will remain paid (eg see Corporate headhunters)
 * Added debugging functionality and hooks based on verbosity setting. Should make my life easier from now on.
 * Autoscript for discarding cards from hand.
 * Automatic Damage prevention can now be switched on/off
 * Actions for damage now take account damage prevention
 * Added a way for cards with abilities on access to be activated by the corp even when unrezzed.
 * New modulator -onlyforDummy which restricts an ability only for Dummy cards.
 * Fixed a bug when trying to use abilities on Dummy cards
 * Fixed a bug when trying to find a marker by its mdict keyname
 * CreateDummy will now inform to pass control if the Dummy card is for the opponent
 * InflictX now works though atTurnStart/End (e.g. Cerberus)
 * Fixed the Agenda scoring checking the advance counters against the wrong number.
 * Made hidden resources work normally for auto-actions
 
### 2.1.6 

Fixed some regression bugs on the autoscripts.  You'll need to download the new patch.

### 2.1.5 

Disabled the debug option ;)

### 2.1.4

* Fixed bug with Deal with Militech and added an Autotargeting autoscript mechanism.

### 2.1.3

Implemented the custom cards which have some of the more unique effects. With this all the core set is truly completed (as much as possible that is)

* Microtech AI Interface
* Crash Everett, Inventive Fixer
* New Blood
* Dr. Dreff
* Social Engineering
* Corporate War
* Mystery Box

### 2.1.2

First version with full automation for most cards in the basic set. From adding markers when you play them, to fully automatizing Arasaka Owns You and Emergency Self-Construct ;)
Changes and bugfixes far too numerous to mention. Needless to say this is a huge update. 

At this moment only the core set is such automated. The other sets are still usable but might need to edit their definitions to make them compatible (Will release a patch)

### 2.0.8.2

* No more crashing scripts when player closes windows that ask for numbers
* Increased the chat font-size to 11 to be more visible on high resolutions (eg 1920x1080)

### 2.0.7

* Added ? character on the chatbox, when the player takes an action, to be able to distinguish those notifications better.
  * Important, because of the above change, you'll have to delete your old chat fonts if you're on windows XP and see a square instead of the Enter character. Simply delete the ```%USERPROFILE%\My Documents\Octgn\Games\13568561-7a2e-4572-8f31-3d99580ab245\cmd64.ttf``` file.
* Paying Action now take into account your max actions (as modified by cards and the player) 
* Cards that have the "double" trait now correctly use two actions when played. (Toon)
* Fixed some wonky indentations.
* Replaced "Note:" with ":::Warning:::" to make them stand out more.
* Playing Hardware Deck or Unique cards now will confirm and trash existing such cards of the player (Toon)
* Player will now be prevented from drawing cards automatically if they have an effect which modifies the amount of cards they draw each time. (Toon)
* Added action to check errata and rulings for a card on netrunneronline.com (Toon)
* Added more autoscripting. (Toon)
  * Runs
  * Losing tags
  * Rolling Dice
  * Refilling Hand
  * Increasing your Actions Max.


### 2.0.6

* Changed chat font size to 10 and menu size to 11

### 2.0.5.3

* Made +1 and -1 card markers counter each other.
* Added two extra markers. Generic and Advance (Toon)
* Added two extra autoscripts for adding extra actions and generic counters (Toon)
* Added a function to add any kind of marker.
* Made deck checking work robustly in multiplayer

### 2.0.4

* Added custom fonts to be used with OCTGN 3.0.1.4

### 2.0.3

* Fixed automations for cards like Cortical Cybermodem.


### 2.0.2

* Cards with MU cost now announce how much it is when they installed, and return it back to their owner when they're trashed.
* Fixed +MU card giving double the bonuses.

### 2.0.1

* Agenda scoring should now work for the runner.
* Fixe bug where Corp Upgrades were being installed face-up
* Put a warning in case people try to start a game without a two-sided-table
* Scored agendas now moved to the scoring player's side and stacked.

### 2.0.0

The latest release of the co-operation between Db0 and toon. Netrunner 2.0.0 is released!

* Autoscripts are now working without errors. This means that many of the cards that do something fairly simple, like drawing 3 cards, or increasing your handsize, now do that automatically.
* Function to disable Autoscripts in the game menu
* New each card has only one "Keywords" field instead of 5 separate ones. This means that filtering cards by their traits is much easier in the deck editor. This will require [a patching of your existing sets](https://github.com/downloads/db0/Netrunner-OCTGN/Patch_2.0.0.o8p)

Due to the significant changes in this version, it is strongly suggested that you delete your OCTGN\Database folder after patching. OCTGN should automatically reinstall all your games the next time you start it (If not, just go to options, select Install on Launch and restart OCTGN)
Don't forget to download the latest markers file as well.

Also keep in mind that the current (as of 20/04/2012) stable versions of OCTGN do not support the custom fonts that are enabled by the game. If you see squares where you should be seeing characters, (or if you just want to experience the awesomeness) use the [OCTGN Beta 4](https://github.com/downloads/Gravecorp/OCTGN/beta4.zip).

### 1.5.11

* Added Commodore 64 fonts for the chat box

### 1.5.10

* Added modified [Cyberpunks Not Dead font](http://www.dafont.com/cyberpunk-is-not-dead.font) (with some specific unicode support). many thanks to Aurelius :-)
* Changed some wordings.
* Agenda Points scored now visible on player summary.
* Changed the hand "Trash Card" actions to "Trash/Archive" to be more descriptive. 
* "Move to Archives H" now is "Move to Face-Up Archives" since the Hidden archives are alread delt with the normal "Trash/Archive".

### 1.5.9

* Renamed some option to be more thematic
* Converted all bit references to unicode via new function
* Reworked the automation ON/OFF to use boolean and to be smaller.
* Added option to switch unicode bits on/off
* Added Unicode font as default to be used in the upcoming version of OCTGN(untested)

### 1.5.8

* Fixed playing or rezzing cards at no cost not putting it on the table.

### 1.5.7

* Fixed the card placing for a 2-player inverted table setup.

### 1.5.6

* Disabled Automations so that the game can be playable until they are finalized

### 1.5.5

* Made The "Declare Start of Turn", "Declare End of Turn" more central to the game. It supposed to work as follows
  * At the start of your turn, you press F1 to declare the start of your turn. This also reinitializes your actions and makes some further checks for mistakes
  * When you're done with your turn, you press F12 to declare the end of your turn. It does some further checks and if it realizes that you have more cards in your hand than your handsize, it puts you in the "End Turn Phase" where you have to discard your excess cards
  * When done with discarding, you press F12 again and after some internal checks, the game announces the end of your turn.
* The mandatory draw action has been removed as its own unique entity. It has been merged into the normal card draw action, but to work correctly you need to use the end turn, start turn actions appropriately.
* Added more unicode Action and Bit characters on the menu!
* Now runs, paying to remove traces and paying to discard resources costs an action
* Added action to change your Action limit per turn. THis is used when they are automatically refreshed at Turn Start.
* Added new hand action for card discard. This automatically places the cards in the right pile depending if you're corp or runner. It also shows thematic messages when done during the end-of-turn phase.

### 1.5.4

* Reorganized the context menu for the table
* Now drawing a card uses an action. Playes can use the Draw Many option to avoid this.
* Advancing a card now uses propely the payCost() and useAction() functions
* Muted some trace functions
* Added function for players to use an action and get a bit
* Started using unicode "Return" character to denote which options require the use of an Action.
* Started using unicode [Dingbats](http://www.alanwood.net/unicode/dingbats.html) 10102 to 10111 to denote which options require the payment of bits. The getBit() function also uses them in its message.
* Removed the Brain damage counter and now using only the hand size one. The hand size counter has the brain icon now.

### 1.5.3

* Changed placement of various cards for corp and runner to make more use of the board setup
* Renamed the "Trash" to "Trash/Archives(face-up)" and "Archives" to "Archives(Hidden)"

### 1.5.2

* Trimmed down the unused actions
* Implemented a better Actions notification, based on the Actions counter. When player does not have enough default actions, they will be warned. 
* Superfluous "Action #2","Action #3" etc removed in favour of a single "Declare Action" action.
* When a player plays a card from their hand, the game automatically uses an action.
* Implemented a new payCost() function that takes care of reducing the player's Bit Pool and informing if that's not possible.
* Made card payment go through the payCost action. This takes into accound "play for free" actions
* Added Ctrl+Shift+S shortcut to Setup Game.
* Archives H renamed to Archives
* Archives renamed to Trash
* Rez and Trash actions now properly use the payCost() function
* Modified the placement of the corp's 3 starting data forts cards.


### 1.5.1

* New intPlay() function that is more consise but has the same functionality.
* Fixed issues with modifying counters and generally integers not being converted
* Changed some calls to counters to their shorthand names for better readability

### 1.5.0

* Fork in github of the work done by Toon offline. This version included more automation, particularly when playing cards.

### 1.0.0

* Initial version uploaded to OCTGN forums. Compatible with OCTGN2. Made by Toon & Firwally.
