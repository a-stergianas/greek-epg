<div align="center">

# 📺 Greek EPG

**Ελληνικός και κυπριακός τηλεοπτικός οδηγός για IPTV**

Πρόγραμμα από πολλαπλές πηγές, συγκεντρωμένο σε ένα XMLTV με σταθερό URL.

![XMLTV](https://img.shields.io/badge/format-XMLTV-2563eb?style=flat-square)
![7 days](https://img.shields.io/badge/window-7_days-7c3aed?style=flat-square)
![12 hours](https://img.shields.io/badge/refresh-12h-16a34a?style=flat-square)
![GitHub Pages](https://img.shields.io/badge/hosting-GitHub_Pages-111827?style=flat-square)

[📥 XMLTV](https://a-stergianas.github.io/greek-epg/epg.xml) ·
[🗜️ Συμπιεσμένο XMLTV](https://a-stergianas.github.io/greek-epg/epg.xml.gz) ·
[📊 Κατάσταση & κάλυψη](https://a-stergianas.github.io/greek-epg/status.json)

</div>

## 🚀 Πρόσθεσέ το στον player σου

Αντέγραψε το παρακάτω URL στη ρύθμιση **EPG / XMLTV / Οδηγός προγράμματος** της εφαρμογής σου:

```text
https://a-stergianas.github.io/greek-epg/epg.xml
```

1. Πρόσθεσε το URL ως πηγή EPG και αποθήκευσε τη ρύθμιση.
2. Πάτησε **Ενημέρωση EPG** ή την αντίστοιχη επιλογή της εφαρμογής.
3. Αν κάποιο κανάλι δεν αντιστοιχιστεί αυτόματα, αντιστοίχισέ το χειροκίνητα με το κανάλι του οδηγού. Στις λίστες M3U, το `tvg-id` πρέπει να συμφωνεί με το `id` του καναλιού στο XMLTV.

Για εφαρμογές που υποστηρίζουν συμπίεση gzip, μπορείς να χρησιμοποιήσεις το μικρότερο αρχείο:

```text
https://a-stergianas.github.io/greek-epg/epg.xml.gz
```

## 📦 Διαθέσιμα αρχεία

| Αρχείο | Περιεχόμενο |
| --- | --- |
| [epg.xml](https://a-stergianas.github.io/greek-epg/epg.xml) | Ο τηλεοπτικός οδηγός σε XMLTV, με κωδικοποίηση UTF-8. |
| [epg.xml.gz](https://a-stergianas.github.io/greek-epg/epg.xml.gz) | Το ίδιο XMLTV, συμπιεσμένο με gzip. |
| [status.json](https://a-stergianas.github.io/greek-epg/status.json) | Ημερομηνία συλλογής, πλήθος καναλιών και εκπομπών, χρονικό εύρος και κάλυψη ανά κανάλι. |

## 🗓️ Επτά ημέρες προγράμματος

Κάθε συλλογή καλύπτει **τη σημερινή ημέρα, τις 3 προηγούμενες και τις 3 επόμενες**, με βάση τη ζώνη ώρας `Europe/Athens`.

| −3 ημέρες | −2 ημέρες | −1 ημέρα | Σήμερα | +1 ημέρα | +2 ημέρες | +3 ημέρες |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Παρασκευή 9 | Σάββατο 10 | Κυριακή 11 | **Δευτέρα 12** | Τρίτη 13 | Τετάρτη 14 | Πέμπτη 15 |

*Ενδεικτικό παράδειγμα όταν σήμερα είναι Δευτέρα 12 του μηνός.*

Η διαθέσιμη κάλυψη εξαρτάται από το πρόγραμμα που δημοσιεύει κάθε πηγή. Το ιστορικό των συλλογών διατηρείται για να υποστηρίζει τις προηγούμενες ημέρες. Όπου δεν υπάρχουν πραγματικά δεδομένα, παραμένουν κενά.

## 🔄 Αυτόματη ενημέρωση

- Η συλλογή προγραμματίζεται **δύο φορές την ημέρα, ανά 12 ώρες**, μέσω GitHub Actions.
- Τα δεδομένα συγχωνεύονται με προτεραιότητες ανά κανάλι και διαθέσιμες εφεδρικές πηγές.
- Το αποτέλεσμα δημοσιεύεται αυτόματα στο GitHub Pages, αφού ολοκληρωθούν η συλλογή και οι έλεγχοι.
- Τα URLs παραμένουν σταθερά, ώστε ο player να λαμβάνει τις επόμενες εκδόσεις από την ίδια διεύθυνση.
- Αν η συλλογή αποτύχει στους ελέγχους δημοσίευσης, παραμένει διαθέσιμη η προηγούμενη έγκυρη έκδοση.

Η ώρα ολοκλήρωσης μπορεί να διαφέρει ανάλογα με τη διαθεσιμότητα των πηγών και τον χρόνο εκτέλεσης. Ενεργοποίησε και την αυτόματη ανανέωση EPG στον player σου, εφόσον την υποστηρίζει.

## 📊 Κάλυψη και κενά

Στο [status.json](https://a-stergianas.github.io/greek-epg/status.json) μπορείς να δεις:

- `generated_at`: τη χρονική σήμανση έναρξης της δημοσιευμένης συλλογής, σε UTC.
- `window`: το χρονικό διάστημα του οδηγού.
- `channels` και `programmes`: το πλήθος καναλιών και εκπομπών της συγκεκριμένης έκδοσης.
- `channel_coverage`: την κάλυψη κάθε καναλιού και τις ημέρες με διαθέσιμα δεδομένα.
- `missing_channels` και `insufficient_days`: κανάλια χωρίς εκπομπές και ημέρες με ελλιπή κάλυψη.

Το `partial: true` σημαίνει ότι υπάρχουν κενά στην κάλυψη. Μια επιτυχημένη δημοσίευση μπορεί να περιέχει τέτοια κενά· οι ελλείψεις των πηγών καταγράφονται χωρίς να προστίθενται επινοημένες εκπομπές.

<details>
<summary><strong>🔗 Πηγές τηλεοπτικού προγράμματος</strong></summary>

Η συλλογή συνδυάζει επίσημους οδηγούς καναλιών και οδηγούς παρόχων. Η πηγή που χρησιμοποιείται διαφέρει ανά κανάλι και διαθεσιμότητα.

| Κατηγορία | Πηγές |
| --- | --- |
| Οδηγοί Ελλάδας | [Digea](https://www.digea.gr/el/tileoptikoi-stathmoi/ilektronikos-odigos-programmatos) · [ERTFLIX](https://www.ertflix.gr/#/guide) · [ANT1](https://www.antenna.gr/tvguide) · [MagentaTV](https://www.magentatv.gr/program) · [Nova](https://epg.nova.gr/) |
| Ελληνικά κανάλια | [ALPHA](https://www.alphatv.gr/programma/) · [ΣΚΑΪ](https://www.skai.gr/tv/programma) · [OPEN](https://www.tvopen.gr/schedule) · [STAR](https://www.star.gr/tv/programma) · [MEGA](https://www.megatv.com/tv-program/) |
| Αθλητικά | [ΣΠΟΡ FM TV](https://www.sportfmtv.gr/el/guide) |
| Παιδικά | [Disney Channel](https://tv.disney.gr/whats-on) · [Disney Junior](https://tv.disney.gr/whats-on/disney-junior) · [Baby TV](https://tv.disney.gr/whats-on/baby-tv) |
| Ντοκιμαντέρ | [National Geographic](https://www.natgeotv.com/gr/schedule/natgeo) · [National Geographic Wild](https://www.natgeotv.com/gr/schedule/nationalgeographicwild) |
| Ψυχαγωγία | [FX](https://www.fxchannel.gr/schedule/fx) · [FX Life](https://www.fxchannel.gr/schedule/fxlife) |
| Κύπρος | [Cyta / Cytavision](https://epg.cyta.com.cy/tv-guide/el) · [Cablenet](https://cablenet.com.cy/tv/tv-guide/) · [ΡΙΚ](https://tv.rik.cy/schedule/) |
| Mesimvria | [Movies Best HD](https://www.mesimvria.com/channel/movies-hd/) · [Greek Cinema](https://www.mesimvria.com/channel/greek-cinema/) · [Cablenet Cinema](https://www.mesimvria.com/channel/cablenet-showtime-1-hd-2/) |

</details>

---

<div align="center">

**Ένα URL στον player σου. Αυτόματη ανανέωση του τηλεοπτικού οδηγού.**

</div>
