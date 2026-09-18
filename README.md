# 🧬 MyHeritage DNS Triangulációs és Ág-kereső Eszköz / DNA Triangulation & Branch Finder

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/pandas-2.0%2B-150458.svg)](https://pandas.pydata.org/)
[![AI Powered](https://img.shields.io/badge/AI-Powered%20by%20Gemini-orange.svg)](https://deepmind.google/technologies/gemini/)

---

<details open>
<summary><b>🇭🇺 Magyar nyelvű leírás (Kattints a kinyitáshoz/bezáráshoz)</b></summary>

<br>

Ez a projekt a **MyHeritage** által exportált DNS-szegmens adatok feldolgozását, egyesítését és elemzését automatizálja. A fejlesztés a **trianguláció (háromszögelés)** genetikális elvére épül: segítségével meghatározható, hogy egy ismeretlen rokon az **apai-nagyapai** vagy az **apai-nagyanyai** (vagy egyéb specifikus) felmenői ághoz tartozik-e.

> 🤖 **Megjegyzés:** A projekt kódbázisa és dokumentációja **Mesterséges Intelligencia (AI)** közreműködésével és támogatásával készült.

---

### 🛠️ Fő funkciók

* **`egyesito.py` (CSV Összefűző)**
  * A MyHeritage korlátozását áthidalva (amely egyszerre legfeljebb 7 rokon közös szegmenseit engedi letölteni) korlátlan számú letöltött `.csv` fájlt egyesít egyetlen master adatbázisba (`Shared_DNA.csv`).
  * Automatikus karakterkódolás-felismerés (UTF-8-SIG, UTF-8, ISO-8859-2, CP1250 stb.).
  * Fejlécek és duplikált adatsorok automatikus tisztítása.

* **`dna_ag_elemzo.py` (Ág-kereső és Triangulátor)**
  * **Ékezet- és kis/nagybetű-független keresés:** A magyar és nemzetközi ékezetes neveket automatikusan normalizálja.
  * **Horgony-rokonok (Anchor Matches) kezelése:** Ismert felmenőjű rokonok hozzárendelése konkrét családfa-ágakhoz (pl. `apai-nagyapai`).
  * **Kromoszóma átfedés elemzés:** Szegmensről szegmensre vizsgálja a kezdő és záró pozíciók átfedését a megadott célszemélynél.
  * **Eredmény-összegzés:** Kiértékeli az átfedő szegmensek számát és meghatározza a legvalószínűbb származási ágat.

---

### 🚀 Használat

#### 1. Előfeltételek
Győződj meg róla, hogy a Python 3 és a `pandas` csomag telepítve van:

```bash
pip install pandas
