# Grundlagen-der-KI-Praktika1-
Search.03 "Dominanz"
Eine Heuristik h₁(n) dominiert eine andere Heuristik h₂(n),
wenn sie immer größer oder gleich ist als h₂(n), aber trotzdem zulässig bleibt.
„Zulässig“ bedeutet, dass die Schätzung nie zu groß ist sie darf den echten Restweg also nicht überschätzen.

Man kann sagen:
h₁ ist besser, weil sie genauere Schätzungen liefert
h₂ ist schwächer, weil sie weniger Informationen hat
Wirkung in A*:
Wenn A* eine dominierende Heuristik benutzt,
findet sie das Ziel schneller,
weil sie weniger nutzlose Wege ausprobiert
Sie spart also Zeit und Speicher,
aber findet trotzdem den gleichen optimalen Weg wie vorher.

Beispiel:
h₂(n) = 0 → das bedeutet: keine Ahnung, wie weit es noch ist (wie Dijkstra).
h₁(n) = Luftlinie zum Ziel → bessere Schätzung, also dominiert h₂.
Mit h₁ prüft A* nur Wege, die wirklich Sinn machen,
während mit h₂ alles durchsucht werden muss
Dadurch ist die Suche mit h₁ viel effizienter




Search.04 – Optimalität von A*

A* gilt als optimaler Suchalgorithmus,
wenn die verwendete Heuristik zulässig ist 
das heißt: sie überschätzt nie die echten Kosten bis zum Ziel.

A* berechnet für jeden Knoten den Wert:
𝑓(𝑛)=𝑔(𝑛)+ℎ(𝑛)
f(n)=g(n)+h(n)

g(n): Kosten vom Start bis zum aktuellen Punkt

h(n): geschätzte Kosten bis zum Ziel

A* wählt immer den Knoten mit dem kleinsten f(n).
Dadurch wird zuerst der Weg untersucht,
der am wahrscheinlichsten zum Ziel führt.

Wenn A* das Ziel erreicht
kann man sicher sein,
dass kein anderer Weg günstiger ist.

Kurz gesagt:
Wenn die Heuristik gut und zulässig ist,
findet A* immer den besten Weg 
also optimal und sicher.
