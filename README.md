# Planitapp Összes

Ez a repository tartalmazza az összes fájlt, beleértve a [planit-vizsgaremek-fullstack](https://github.com/janoscsordas/planit-vizsgaremek-fullstack) repository-t, illetve a weboldalhoz készített [dokumentációt](https://github.com/janoscsordas/planit-vizsgaremek-dokumentacio) bemutató repository-t is.

A két repository-t [submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules)-ként fűztük hozzá ehhez a repository-hoz.

## Projekt struktúra
- **assets**: Tartalmazza a projekt adatbázis-szerkezetét .svg fájlban
- **planit-vizsgaremek-dokumentacio**: Planitapp-dokumentáció submodule
- **planit-vizsgaremek-fullstack**: Planitapp-fullstack submodule
- **LICENSE**: Tartalmazza az MIT license-t

## Telepítési útmutató

### Repository klónozása submodule-okkal együtt

```bash
git clone --recurse-submodules https://github.com/janoscsordas/planit-vizsgaremek-osszes
cd planit-vizsgaremek-osszes
```

### Már clone-ozta a repository-t, de a submodule-ok még hiányoznak

```bash
git submodule init
git submodule update
```

### Submodule-ok frissítése a legfrissebb verzióra

```bash
git submodule update --recursive --remote
```

## Fejlesztési irányelvek

A fejlesztés során az egyes komponensekben végzett módosításokat az eredeti repository-kba (planit-vizsgaremek-fullstack, planit-vizsgaremek-dokumentacio) kell push-olni. Ezután a fő repository-ban frissíteni kell a submodule referenciákat:

```bash
# A submodule-okban végzett módosítások után
cd planit-vizsgaremek-osszes
git add planit-vizsgaremek-fullstack
git add planit-vizsgaremek-dokumentacio
git commit -m "Update submodule version"
git push
```

## Licenc

[MIT](LICENSE)
