# Ilm Library Netlify Category Repair

Verified the latest Netlify build and found a real issue: the Categories page counted Quran as a normal book category, but the books dataset contained no item whose category was exactly `Quran`. As a result, the Quran category displayed 0 books and its category page was empty.

Repair:
- Added a dedicated Quran category card.
- The card links directly to the working `#quran` Surah list.
- It displays 114 Surahs / 6,236 Ayahs.
- Added a dedicated Quran category page so `#category&name=Quran` is never empty.
- Kept the existing card/button styling and added only minimal spacing for the new action button.
- Existing non-Quran category behavior was left unchanged.
- JavaScript syntax check passes after the repair.
