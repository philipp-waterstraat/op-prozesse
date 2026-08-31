# OP-Prozesszeiten

Interaktive Darstellung der perioperativen Prozesszeitpunkte und Kennzahlen entlang
des tatsächlichen Ablaufs im OP-Bereich.

**→ [Anwendung öffnen](https://philipp-waterstraat.github.io/op-prozesse/)**

---

## Wozu

Prozesskennzahlen im OP sind Zeitintervalle zwischen zwei dokumentierten Ereignissen.
Dieser Zusammenhang ist im Gespräch schwer zu vermitteln, besonders gegenüber
Beteiligten, die nicht täglich im OP arbeiten.

Die Anwendung macht ihn sichtbar: Ein Klick auf eine Kennzahl hebt genau die beiden
Zeitpunkte hervor, aus denen sie gebildet wird. Umgekehrt zeigt das Überfahren eines
Zeitpunkts alle Kennzahlen, die auf ihm aufbauen.

## Was sie enthält

- **39 Zeitpunkte** aus Patientenlogistik, Anästhesie, Operation und Saallogistik
- **27 fallbezogene Kennzahlen**, gegliedert nach Prozessverantwortung statt nach Fachgebiet
- **12 Zusatzintervalle**, die im Glossar nicht konsentiert sind, im Alltag aber gemessen werden
- **16 Kapazitäts- und Auslastungskennzahlen** in einer eigenen Ansicht

## Funktionen

**Prozessvarianten.** Ort der Anästhesie-Einleitung (Einleitungsraum, OP-Saal,
zentral überlappend) und Ort der Ausleitung (OP-Saal, Ausleitungsbereich) sind
umschaltbar. Die Varianten ändern die Berechnung: Bei Einleitung außerhalb des Saals
beginnt der Operative Vorlauf mit *Patient im OP-Saal* statt mit *Freigabe Anästhesie*,
und bei Ausleitung im Ausleitungsbereich entfällt die Bindung des OP-Funktionsdienstes
in der Ausleitungsdauer.

**Berufsgruppenfilter.** Auswählbar nach zeitlicher Bindung oder nach
Prozessverantwortung, in drei Modi: *beteiligt*, *ausschließlich* und *gemeinsam mit
anderen*. Damit lässt sich etwa zeigen, in welchem Fenster nachweislich nur die
OP-Pflege am Patienten arbeitet, oder wo genau die Schnittstellen zwischen den
Berufsgruppen liegen.

**Parallelprozesse.** Zu jeder Kennzahl lassen sich alle Intervalle einblenden, die
sich zeitlich mit ihr überschneiden.

**Hauskonfiguration.** Zwei Zuständigkeiten sind hausindividuell geregelt und deshalb
einstellbar: wer das Einschleusen verantwortet und wer die nachsorgende Einheit
anmeldet. Die Einstellung steht im Adressfragment und lässt sich als Lesezeichen oder
Link pro Einrichtung ablegen.

**Darstellung.** Hell- und Dunkelmodus, zuschaltbare Beschriftungen, Präsentationsgröße,
Befehlspalette über `Strg`/`Cmd` + `K`, sowie eine Druckausgabe für A3 quer.

## Technik

Eine einzelne HTML-Datei ohne Abhängigkeiten. Schriften sind eingebettet, es werden
keine externen Ressourcen nachgeladen, keine Cookies gesetzt und keine Analyse- oder
Trackingdienste eingebunden. Die Datei funktioniert per Doppelklick auch ohne
Internetverbindung und lässt sich unverändert per E-Mail weitergeben.

Alle Zeitpunkte und Kennzahlen liegen als Datenmodell vor; die Grafik wird daraus zur
Laufzeit als SVG erzeugt. Eine Änderung an einer Definition betrifft damit genau eine
Stelle.

## Datengrundlage

Ein Großteil der Zeitpunkte und Kennzahlen beruht auf dem Glossar perioperativer
Prozesszeiten und Kennzahlen in der Version 2020. Bezeichnungen und Codes sind die dort
konsentierte Fachterminologie; die Erläuterungstexte sind eigene Formulierungen und
keine wörtliche Wiedergabe.

Die Darstellung folgt bewusst dem tatsächlichen Prozess und nicht ausschließlich dem
Regelwerk. Wo im Glossar für einen real messbaren Vorgang keine Kennzahl vorgesehen ist,
etwa für die Saalreinigung, das Warten auf den Operateur oder den Rückweg des
Anästhesisten, ist ein Zusatzintervall ergänzt. Diese sind in der Anwendung
gekennzeichnet und im Detailpanel jeweils mit dem Hinweis versehen, warum das Glossar
an dieser Stelle keine Kennzahl vergibt.

Zeitpunkte, die keine Glossar-Kennzahl aufspannen, tragen in der Grafik eine eigene
Markierung. So bleibt erkennbar, was das Regelwerk offenlässt.

### Quellen

> Bauer M, Auhuber TC, Kraus R, Rüggeberg J, Wardemann K, Müller P, Taube C, Diemer M,
> Schuster M: Glossar perioperativer Prozesszeiten und Kennzahlen. Eine gemeinsame
> Empfehlung von BDA, BDC, VOPM, VOPMÖ und SFOPM. Version 2020.
> *Anästh Intensivmed* 2020;61:516–531. DOI: [10.19224/ai2020.516](https://doi.org/10.19224/ai2020.516)

> Bauer M, Schuster M: Prozesszeiten und Kennzahlen im OP-Management.
> *OP-Management up2date* 2021;1:63–82. DOI: [10.1055/a-1335-7759](https://doi.org/10.1055/a-1335-7759)

## Verwendung

Die Anwendung ist über den Link oben direkt aufrufbar. Alternativ lässt sich
`index.html` herunterladen und lokal öffnen, der Funktionsumfang ist identisch.

Für eine Aktualisierung wird `index.html` im Repository ersetzt; GitHub Pages
veröffentlicht die neue Fassung innerhalb weniger Minuten.

## Rechtliches

Impressum und Datenschutzerklärung sind über die Fußzeile der Anwendung erreichbar.
Das Angebot wird privat und ohne Gewinnerzielungsabsicht bereitgestellt.

Konzeption, Datenmodell, Texte und Programmcode sind unter Verwendung von Claude,
einem KI-Assistenten der Anthropic PBC, entstanden. Fachliche Auswahl, Prüfung und
Verantwortung liegen beim Autor.

## Autor

Philipp Waterstraat, MSc. Prozessmanagement und Consulting, mit Hintergrund in
OP-Pflege und OP-Management.
