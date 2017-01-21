# Mietvertrag Vorlage

Dieses Muster kann als Grundlage für einen Mietvertrag verwendet werden.

Der in rot markierte Text muss entsprechend angepasst werden. Die meisten Werte
sind als `\newcommand` erfasst und können zentral geändert werden, wie z.B. der
Name des Vermieters.

    \newcommand{\vermieter}{\textcolor{zuBearbeiten}{Max Mustermann}}

Die anderen Bereiche müssen in der Vorlage selbst angepasst werden, wie z.B.
die Anzahl der zu vermietenden Räume.

Sind alle Anpassungen abgeschlossen, sollte folgender Parameter von

    \definecolor{zuBearbeiten}{RGB}{255, 0, 0}

auf

    \definecolor{zuBearbeiten}{RGB}{0, 0, 0}

geändert werden, um die Farbe des Textes von rot wieder auf schwarz zu ändern.

## MacOS Voraussetzungen

Um das Template unter MacOS übersetzen zu können muss
[MacTex](https://tug.org/mactex/) installiert sein.

## PDF Erzeugung

Um aus dem LaTeX Quelltext ein PDF zu erzeugen wechselt man am besten in einem
Terminal Fenster in den Ordner in dem der Mietvertrag gespeichert wurde. Wurde
der Mietvertrag z.B. im Ordner `~/Dokumente/Mietvertrag` gespeichert verwendet man
im Terminal:

    cd ~/Documents/Mietvertrag

Das PDF kann anschliessend mit folgendem Kommando erzeugt werden:

    for i in $(seq 1 2); do pdflatex -interaction=batchmode Mietvertrag.tex; done

Der Mietvertrag kann dann mit folgendem Befehl geöffnet werden:

    open Mietvertrag.pdf
