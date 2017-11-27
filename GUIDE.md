## What you need to make OpenTibia Sprite Pack work!

OpenTibia Sprite Pack (OTSP) uses different IDs for everything.

#### Engine
- default OTSP protocol is 10.41, make sure your engine is downgraded or that you change OTSP files protocol;
- different effects and IDs, you might want to change tons of stuff at const.h source file ([here](https://github.com/otland/forgottenserver/blob/master/src/const.h#L434-L484));
- maybe you would want to change effects name to reflect current ones, it would change how you make spells and monsters spells ([here](https://github.com/otland/forgottenserver/blob/eeacf88c1139d9eb9924e77b8e31deb02c284d41/src/tools.cpp#L507-L641));
- CONST_ME_TELEPORT and other ones are used in a lot of places in the code, you might want to change that ([here](https://github.com/otland/forgottenserver/search?l=C%2B%2B&q=CONST_ME_TELEPORT&type=&utf8=%E2%9C%93));

#### Data
- you will need to change actions/movements/weapons for OTSP items ids;
- change Doors at global.lua ([here](https://github.com/otland/forgottenserver/blob/master/data/global.lua#L7-L13));
- create totally new spells using OTSP effects;
- create totally new monsters using OTSP outfits;
- add the outfits to outfits.xml ([here](https://github.com/otland/forgottenserver/blob/master/data/XML/outfits.xml));
- add more details and custom information to our items.xml;

#### Client
- make sure it search for otsp.spr and otsp.dat files instead of deafult ones ([here](https://github.com/edubart/otclient/blob/master/modules/game_things/things.lua#L12));

#### Website/AAC
- check starting outfit and starting items ids (we have outfits from 1-24, 17-21 better suited for players);

#### Tools
- ItemEditor: https://github.com/ottools/ItemEditor
- ObjectBuilder: https://github.com/ottools/ObjectBuilder