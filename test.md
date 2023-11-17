```sh
pkg update
pkg upgrade
pkg i git
pkg i gh
```
**Android**: /storage/emulated/0/obsidian
**PC**: C://Users/.../Desktop/obsidian
```sh
cd /storage/emulated/0/obsidian
git init
git remote add origin ССЫЛКА
git pull
```

Obsidian.sh
```sh
#!/bin/bash
cd /data/data/com.termux/files/home/storage/shared/obsidian
a=$(git pull && git add -A && git commit -a -m "android vault backup: `date +'%Y-%m-%d %H-%M-%S'`" && git push origin main && git pull origin main)
termux-notification --content Success
termux-toast $a
```

```SH
# step by step
cd /data/data/com.termux
cd files
# error: mkdir НАЗВАНИЕ_ПАПКИ
cd home
cd storage
cd shared
cd obsidian

КОПИРОВАНИЕ:
cp СТАРЫЙ_ПУТЬ НОВЫЙ_ПУТЬ
cp /storage/emulated/0/obsidian/obsidian.sh /data/data/com.termux/.shortcuts/
```


Колауты

> [!info] Test
> Lorem ipsum dolor sit ammet
[[test link]]

![[test embedded link]]