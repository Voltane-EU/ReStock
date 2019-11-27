
# ReStock.js <img src="https://cdn.voltane.eu/assets/minecraft/chest_animated.gif" height="50px"/>
__A minimal Loottable Chest or universal Container Refill craftscript__

***

__Want to support us?__

__[☕ Donate a cup of coffee on patreon ](https://www.patreon.com/voltane_eu)__

__[<img src="https://cdn.voltane.eu/logo/icon/icon-hexagon.svg" width="20px" height="25px"/> Contribute to our open-source projects](https://github.com/Voltane-EU)__

__[<img src="https://cdn.voltane.eu/assets/discord/nitro-boost.svg" width="20px" height="25px"/> Boost / Join our Discord server ](https://discord.voltane.eu/)__

__[<img src="https://cdn.voltane.eu/assets/minecraft/grass_block.png" width="20px"/> Join our modded minecraft server ](https://mc.play.voltane.eu/)__

***


<div itemscope itemtype="https://schema.org/FAQPage">
<div itemprop="mainEntity" itemscope itemtype="https://schema.org/Question">
<input id="tab-one" type="radio" name="tabs-faq">
<label itemprop="name" for="tab-one"><h2>Prerequisites</h2></label>
<div itemprop="acceptedAnser" itemscope itemtype="https://schema.org/Answer">
<p itemprop="text">
<em>You will need:</em>
<ul>
<li>A <a href="https://github.com/Voltane-EU/Block-Finder">.json file with an array of container coordinates</a>() that you want to refill.</li>
<li>A <a href="https://minecraft.gamepedia.com/Loot_table">.json loottable</a> (if you want to use a custom loottable).</li>
<li>The <a href="https://enginehub.org/worldedit/">WorldEdit</a> Plugin.</li>
<li>The <a href="https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Rhino/Download_Rhino">Rhino 1.7.11 (or higher)</a> Library.</li>
</ul>
</p>
</div>
</div>

<div itemprop="mainEntity" itemscope itemtype="https://schema.org/Question">
<input id="tab-two" type="radio" name="tabs-faq">
<label itemprop="name" for="tab-two"><h2>Instructions</h2></label>
<div itemprop="acceptedAnser" itemscope itemtype="https://schema.org/Answer">
<p itemprop="text">
<ol>
<li>Install WorldEdit on your Server.</li>
<li>Extract the Rhino Library <code>lib/rhino-{version}.jar</code>.</li>
<li>The <a href="https://enginehub.org/worldedit/">WorldEdit</a> Plugin.</li>
<li>The <a href="https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Rhino/Download_Rhino">Rhino 1.7.11 (or higher)</a> Library.</li>
</ol>
</p>
</div>
</div>

</div>





## Prerequisites
_You will need:_
- A [.json file with an array of container coordinates](https://github.com/Voltane-EU/Block-Finder) that you want to refill.
- A [.json loottable](https://minecraft.gamepedia.com/Loot_table) (if you want to use a custom loottable).
- The [WorldEdit](https://enginehub.org/worldedit/) Plugin.
- The [Rhino 1.7.11 (or higher)](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Rhino/Download_Rhino) Library.

<br/>

## Instructions
1. Install WorldEdit on your Server.
1. Extract the Rhino Library `lib/rhino-{version}.jar`
   - to the `plugins/` or `plugins/WorldEdit` folder on bukkit.
   - to the `mods/` folder on other platforms.
1. Place the craftscript to `%serverroot%/config/worldedit/craftscripts/`.
1. In the same directory create a folder called `restock`.
1. and place your .json container array file into that folder (name it `default.json` if you want to omit the filename on command execution).

<br/>

## Usage
_Command syntax:_\
`/cs restock <namespace/lootTable> <forceReplace> <coordFile>`

__namespace/lootTable [[?]](mcforge.readthedocs.io/en/latest/items/loot_tables/):__
- Which loottable to fill from.
- eg. `mctools:chests/loot_table`

__forceReplace [true|false]:__
- If blocks that aren't the target container should become the target container
```diff
- BE VERY CAREFUL WITH THIS
- TRIPPLE CHECK IF YOUR COORDS ARE CORRECT
- IT CAN'T BE UNDONE!
```
__coordFile [restock/loot]:__
- The file with coordinates of containers to fill (without `.json`)
- You can leave out this argument if your file is called `default.json`.
- Currently the json looks like this: \
`[[54, -70, 28, -118],...] or [[TARGET ID, X, Y, Z],...]`
- Target ID is the Container that you want to fill and/or place at the position
- (I personly only recommend 54 which is a normal chest, but do as you please)
- If you need to generate this file take a look at [this project](https://github.com/Voltane-EU/Block-Finder).

<br/>
