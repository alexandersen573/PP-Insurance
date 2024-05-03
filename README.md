
# Projektname: Versicherungsdatensatz-Analyse

Autoren:
Sarah,
Rick,
Alex

## Beschreibung:
Dieses Projekt befasst sich mit der Analyse eines Versicherungsdatensatzes. Der Datensatz enthält Informationen über Kunden wie Alter, Geschlecht, BMI, Anzahl der Kinder, Raucherstatus, Region und Versicherungskosten. Ziel des Projekts ist es, Einblicke in die Daten zu gewinnen und verschiedene Analysemethoden anzuwenden, um Muster, Trends und Zusammenhänge zu identifizieren.

### Verzeichnisstruktur:
data/: Enthält den Datensatz "20240429_Statistik_Praxisaufgabe_Insurance_Datensatz.csv".
scripts/: Enthält Python-Skripte für Datenanalyse und Visualisierung.
results/: Enthält Ergebnisse der Datenanalyse wie Grafiken, Statistiken usw.
README.md: Diese Datei enthält eine Beschreibung des Projekts.

### Anforderungen:
Matplotlib
NumPy
Pandas
Plotly.express
Python 3
Researchpy
Scipy
Seaborn
Statmodels

#### Ausführung:
Stelle sicher, dass alle erforderlichen Python-Bibliotheken installiert sind.
Führe die Skripte in der Reihenfolge ihrer Nummerierung aus, um die Datenanalyse durchzuführen.
Überprüfe die Ergebnisse in den Ergebnisdateien und führe bei Bedarf weitere Analysen durch.
Hinweis:
Dieses Projekt wird im Rahmen eines Kurses oder einer Praxisaufgabe für Statistik durchgeführt.
Die Analyseergebnisse dienen nur zu Bildungszwecken und können je nach Kontext variieren.

### Erkenntnisse Aufgabe 1:
Skalenniveau der Variablen:
Die Variable "age" hat ein Intervallskalenniveau, was bedeutet, dass sie numerische Werte enthält, die in einem bestimmten Bereich gemessen werden.
"Sex" und "Smoker" sind auf Nominalskalenniveau, was darauf hinweist, dass sie kategorische Variablen sind, die keine Rangordnung haben.
"BMI", "Children" und "Charges" sind auf Verhältnisskala-Niveau, was bedeutet, dass sie numerische Werte haben, bei denen der Abstand zwischen 
den Werten bedeutungsvoll ist und ein echter Nullpunkt vorhanden ist. Umwandlung in niedrigeres Skalenniveau: Das Alter wurde in Altersgruppen umgewandelt,
um die Analyse zu erleichtern und Muster in Bezug auf Altersgruppen zu identifizieren.

Lage- und Streuungsmaße:
Die statistischen Kennzahlen zeigen wichtige Informationen über die 
Verteilung der Daten, wie Mittelwert, Standardabweichung, Minimum, Maximum und verschiedene Perzentile.

Grafische Darstellungen:
Die Histogramme und Boxplots geben visuelle Einblicke in die Verteilung und die möglichen Ausreißer der Variablen wie Alter, BMI, Anzahl der Kinder und Versicherungskosten (Charges).

Zusätzliche Umwandlungen und Visualisierungen:
Es wurden weitere Umwandlungen durchgeführt, um Variablen in Gruppen einzuteilen und diese gruppierten Daten visuell darzustellen.

### Erkenntnisse Aufgabe 2:
In einem ersten Schritt wurden alle Nominalwerte kodiert, um sie für eine Korrelationsanalyse nutzbar zu machen. Ebenfalls wurden zum Zweck der einfacheren Auswertung die Spalte "Region" aufgeteilt in vier Spalten "north", "south", "east" und "west". Dadurch ließen sich genauer Unterschiede zwischen den verschiedenen Regionen ermitteln.

Korrelationsmatrix:
Zuerst wurde mithilfe einer Korrelationsmatrix die Korrelationskoeffizienten innerhalb der Variablenmatrix bestimmt. Hier ließen sich bereits die wichtigesten Erkenntnisse erkennen, die im Anschluss weiter überprüft wurden. Anhand der Heatmap lassen sich drei Variablen identifizieren, die stark positiv mit den Kosten für die Versicherung korrelieren. Diese sind für Raucher (0,787), das Alter (0,299) und der BMI (0,198). Geringere positive Korrelationen mit den Kosten lassen sich bei Personen, die in der östlichen Region leben (0.071), bei Eltern mit Kindern (0.068) und bei Männern (0,057) finden.

Plots:
Bei der bivariaten Analyse der einzelnen Variablen in Bezug auf die Kosten lassen sich einige Erkenntnisse vorab formulieren. Beispielsweise visualisiert das Scatterdiagramms zum Alter und den Kosten deutlich, dass sich drei Preisklassen an Versicherten geben muss, wobei die Kosten mit dem Alter stetig ansteigen. Bei der weiteren deskripitiven Analyse lässt sich feststellen, dass insbesondere Raucher automatisch in höhere Preisklassen fallen und Menschen, mit einem niedrigen BMI kaum in den höchsten Preissegment zu finden sind. Bei der Betrachtung des BMI fällt ebenfalls ein starker Zusammenhang zwischen Rauchern und der Tendenz zu einem hohen BMI auf. Insgesamt lassen sich daher Raucher als wünschenswerte Zielgruppe definieren. Die Einflüsse der anderen Variablen wie, Kinder, Geschlecht und Region sind dagegen relativ klein.

Signifikanz:
Nach der Durchführung der Signifikanztests für die einzelnen Variablen mit der abhängigen Variable "Charges" lässt sich bestätigen, dass insbesondere der Raucherstatus, das Alter und der BMI einen signifikanten Einfluss auf die Kosten haben. Immer noch signifikant aber in einem deutlich geringeren Maße haben das Geschlecht, die Anzahl der Kinder sowie die Region einen Einfluss. Bei der Region scheint es insbesondere ein gefälle zwischen West und Ost zu geben, wobei "east" positiv, und "west" negativ mit höheren Kosten korreliert. 

### Erkenntnisse Aufgabe 3:
Basierend auf unserer Analyse sind Raucher, ältere Personen und Personen mit einem höheren BMI diejenigen, die tendenziell höhere Krankenversicherungsprämien zahlen. Personen in der
Region Southwest und Personen mit Kindern zeigen keine signifikanten Unterschiede in den Prämien im Vergleich zu anderen Regionen und Personen ohne Kinder. Daher könnten wir unsere
Marketingstrategien darauf ausrichten, Raucher und ältere Personen mit einem höheren BMI als potenziell rentable Kunden anzusprechen.



