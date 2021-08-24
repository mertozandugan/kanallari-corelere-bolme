# kanallari-corelere-bolme

>Channel1 Log klasörü oluşturma:
```
cd /usr/game/logs
mkdir channel1
cd channel1
mkdir core1
cd core1
mkdir log
touch PTS
cd ../
cp -R core1 core2
cp -R core1 core3
```

>Diğer kanalların log klasörünü oluşturma:
```
cd /usr/game/logs
cp -R channel1 channel2
cp -R channel1 channel3
cp -R channel1 channel4
cp -R channel1 channel5
cp -R channel1 channel6
```

>Kanal dosyalarını hazırlama:
```
cd /usr/game/cores
mkdir channel1
cd channel1
mkdir core1
cd core1
ln -s ../../../share/data data
ln -s ../../../share/locale locale
ln -s ../../../logs/channel1/core1/log log
ln -s ../../../share/lib/mark mark
ln -s ../../../share/package package
ln -s ../../../share/bin/game ch1core1
ln -s ../../../share/conf/CLIENT_VERSION CLIENT_VERSION
ln -s ../../../share/conf/CMD CMD
ln -s ../../../share/conf/CRC CRC
ln -s ../../../logs/channel1/core1/PTS PTS
ln -s ../../../share/conf/STATE_USER_COUNT STATE_USER_COUNT
touch CONFIG
```

>Diğer core dosyalarını oluşturma:
```
cd /usr/game/cores/channel1
cp -R core1 core2
cp -R core1 core3
cd core2
rm ch1core1
ln -s ../../../share/bin/game ch1core2
rm PTS
ln -s ../../../logs/channel1/core2/PTS PTS
cd ../core3
rm ch1core1
ln -s ../../../share/bin/game ch1core3
rm PTS
ln -s ../../../logs/channel1/core3/PTS PTS
```
>diğer kanal dosyalarını oluşturma:
```
cd /usr/game/cores
cp -R channel1 channel2
cp -R channel1 channel3
cp -R channel1 channel3
cp -R channel1 channel4
cp -R channel1 channel5
cp -R channel1 channel6
```
```
cd channel2/core1
rm ch1core1
ln -s ../../../share/bin/game ch2core1
rm PTS
ln -s ../../../logs/channel2/core1/PTS PTS
cd ../core2
rm ch1core2
ln -s ../../../share/bin/game ch2core2
rm PTS
ln -s ../../../logs/channel2/core2/PTS PTS
cd ../core3
rm ch1core3
ln -s ../../../share/bin/game ch2core3
rm PTS
ln -s ../../../logs/channel2/core3/PTS PTS
```

```
cd ../../channel3/core1
rm ch1core1
ln -s ../../../share/bin/game ch3core1
rm PTS
ln -s ../../../logs/channel3/core1/PTS PTS
cd ../core2
rm ch1core2
ln -s ../../../share/bin/game ch3core2
rm PTS
ln -s ../../../logs/channel3/core3/PTS PTS
cd ../core3
rm ch1core3
ln -s ../../../share/bin/game ch3core3
rm PTS
ln -s ../../../logs/channel3/core3/PTS PTS
```

```
cd ../../channel4/core1
rm ch1core1
ln -s ../../../share/bin/game ch4core1
rm PTS
ln -s ../../../logs/channel4/core1/PTS PTS
cd ../core2
rm ch1core2
ln -s ../../../share/bin/game ch4core2
rm PTS
ln -s ../../../logs/channel4/core2/PTS PTS
cd ../core3
rm ch1core3
ln -s ../../../share/bin/game ch4core3
rm PTS
ln -s ../../../logs/channel4/core3/PTS PTS
```

```
cd ../../channel5/core1
rm ch1core1
ln -s ../../../share/bin/game ch5core1
rm PTS
ln -s ../../../logs/channel5/core1/PTS PTS
cd ../core2
rm ch1core2
ln -s ../../../share/bin/game ch5core2
rm PTS
ln -s ../../../logs/channel5/core2/PTS PTS
cd ../core3
rm ch1core3
ln -s ../../../share/bin/game ch5core3
rm PTS
ln -s ../../../logs/channel5/core3/PTS PTS
```

```
cd ../../channel6/core1
rm ch1core1
ln -s ../../../share/bin/game ch6core1
rm PTS
ln -s ../../../logs/channel6/core1/PTS PTS
cd ../core2
rm ch1core2
ln -s ../../../share/bin/game ch6core2
rm PTS
ln -s ../../../logs/channel6/core6/PTS PTS
cd ../core3
rm ch1core3
ln -s ../../../share/bin/game ch6core3
rm PTS
ln -s ../../../logs/channel6/core3/PTS PTS
```

>*Coreler arası port 10 artış Kanallar arası port 1000 artış şeklinde ilerliyorum.

>auth:
```
PORT					: 11055
P2P_PORT				: 11008
DB_PORT					: 11000
```

>ch1core1:
```
HOSTNAME				: core1
CHANNEL					: 1
PORT					: 13010
P2P_PORT				: 13110
DB_PORT					: 11000
MAP_ALLOW				: 1 3 21 23 25 41 43 45
```

>ch1core2:
```
HOSTNAME				: core2
CHANNEL					: 1
PORT					: 13020
P2P_PORT				: 13120
DB_PORT					: 11000
MAP_ALLOW				: 61 62 63 64 65 66 67 68 69 70 71 72 73 301 302 303 304 351 352
```

>ch1core3:
```
HOSTNAME				: core3
CHANNEL					: 1
PORT					: 13030
P2P_PORT				: 13130
DB_PORT					: 11000
MAP_ALLOW				: 104 108 109 208 216 217
```

>ch2core1:
```
HOSTNAME				: core1
CHANNEL					: 2
PORT					: 14010
P2P_PORT				: 14110
DB_PORT					: 11000
MAP_ALLOW				: 1 3 21 23 25 41 43 45
```

>ch2core2:
```
HOSTNAME				: core2
CHANNEL					: 2
PORT					: 14020
P2P_PORT				: 14120
DB_PORT					: 11000
MAP_ALLOW				: 61 62 63 64 65 66 67 68 69 70 71 72 73 301 302 303 304 351 352
```

>ch2core3:
```
HOSTNAME				: core3
CHANNEL					: 2
PORT					: 14030
P2P_PORT				: 14130
DB_PORT					: 11000
MAP_ALLOW				: 104 108 109 208 216 217
```

>channel99:
```
HOSTNAME				: channel99
CHANNEL					: 99
PORT					: 13099
P2P_PORT				: 13199
DB_PORT					: 11000
MAP_ALLOW				: 81 113 212 103 105 110 111 114 118 119 120 121 122 123 124 125 126 127 128 181 182 183 190 191 192
```
>db:
```
BIND_PORT					= 11000
```

<iframe width="500" height="300" src="https://www.youtube.com/embed/khFogvxsmj8" frameborder="0" allowfullscreen></iframe>
