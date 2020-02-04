# mod-morphsummon

![mod-morphsummon](https://raw.githubusercontent.com/azerothcore/mod-morphsummon/master/icon.png)


Latest build status with azerothcore: [![Build Status](https://travis-ci.org/azerothcore/mod-morphsummon.svg?branch=master)](https://travis-ci.org/azerothcore/mod-morphsummon)


## Important notes

You have to use at least AzerothCore commit [3f0739f](https://github.com/azerothcore/azerothcore-wotlk/commit/3f0739f1c9a5289444ff9d62834b7ceb38879ba9).


## Description

This module allows Warlocks, Death Knights and Mages to alter the appearance of their summoned permanent creatures (incl. the Felguard's weapon). The appropriate model / item IDs can be specified in the configuration file.


## How to use ingame

As GM:
- add NPC permanently:
 ```
 .npc add 601072
 ```
- add NPC temporarily:
 ```
 .npc add temp 601072
 ```


## Installation

Clone Git repository:

```
cd <ACdir>
git clone https://github.com/azerothcore/mod-morphsummon.git modules/mod-morphsummon
```

Import SQL automatically:
```
cd <ACdir>
bash apps/db_assembler/db_assembler.sh
```
choose 8)

Import SQL manually:
```
cd <ACdir>
bash apps/db_assembler/db_assembler.sh
```
choose 4)
```
cd <ACdir>
mysql -P <DBport> -u <DPuser> --password=<DBpassword> world <env/dist/sql/world_custom.sql
```

Without DB Assembler:
```
cd <ACdir>
mysql -P <DBport> -u <DPuser> --password=<DBpassword> world <modules/mod-morphsummon/data/sql/db-world/morphsummon.sql
mysql -P <DBport> -u <DPuser> --password=<DBpassword> characters <modules/mod-morphsummon/data/sql/db-characters/morphsummon_ddl.sql
```


## Edit module configuration (optional)

If you need to change the module configuration, go to your server configuration folder (where your `worldserver` or `worldserver.exe` is), copy `morphsummon.conf.dist` to `morphsummon.conf` and edit that new file.


## Screenshots
![NPC](https://raw.githubusercontent.com/azerothcore/mod-morphsummon/master/images/morphsummon1.jpg "NPC")
![Ghoul](https://raw.githubusercontent.com/azerothcore/mod-morphsummon/master/images/morphsummon2.jpg "Ghoul")
![Felguard](https://raw.githubusercontent.com/azerothcore/mod-morphsummon/master/images/morphsummon3.jpg "Felguard")
![Water Elemental](https://raw.githubusercontent.com/azerothcore/mod-morphsummon/master/images/morphsummon4.jpg "Water Elemental")


## Credits

[Stoabrogga](https://github.com/Stoabrogga): author

AzerothCore: [repository](https://github.com/azerothcore) - [website](http://azerothcore.org/) - [discord chat community](https://discord.gg/gkt4y2x)


## License
This code and content is released under the [GNU AGPL v3](https://github.com/azerothcore/azerothcore-wotlk/blob/master/LICENSE-AGPL3).
