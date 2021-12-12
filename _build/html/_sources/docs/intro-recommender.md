# Recommender

Der Begriff des Recommender Systems oder auch Empfehlungssystem genannt (Klahold, 2009), taucht erstmalig im Jahr 1997 auf und wird von Resnick und Varian (1997) geprägt.

Sie verstanden darunter ein System, welches Empfehlungen von Menschen aggregiert und diese anschließend an einen geeigneten Empfänger weiterleitet (Resnick & Varian, 1997).

Burke (2002) erweitert den Begriff und definiert Empfehlungsdienste wie folgt: „ […] any system that produces individualized recommendations as output or has the effect of guiding the user in a personalized way to interesting or useful objects in a large space of possible options” (Burke, 2002, S.331). 

Aus heutiger Sicht werden darunter Softwareanwendungen und –techniken verstanden, die einem Nutzer Objekte bzw. heutzutage alle Dinge des täglichen Lebens empfehlen (Gärtner, 2012). Für die Generierung von Empfehlungen setzen Empfehlungsdienste Ähnlichkeitsmetriken ein (Höhfeld & Kwiatkowski, 2007). 

Die nachfolgende Abbildung 3 zeigt, wie Eingabedaten mittels einer Empfehlungskomponente, respektive einer Empfehlungstechnik in eine Objektausgabeliste umgewandelt werden. 

Eingabedaten könnten z.B. Benutzermodelle, Produktdaten oder Wissensmodelle sein. Die Objektausgabeliste setzt sich aus den einzelnen Objekten und deren Rang zusammen. Der Rang drückt dabei aus, wie nützlich ein Objekt für den jeweiligen Benutzer ist (Jannach, 2012). 

Formell lässt sich ein Recommender System wie folgt definieren: „[…] ein System, das einem Benutzer in einem gegebenen Kontext aus einer gegebenen Entitätsmenge aktiv eine Teilmenge ‚nützlicher‘ Elemente empfiehlt“ (Klahold, 2009, S.1). 

Der Kontext setzt sich dabei aus dem __Benutzerprofil P__, der __Entitätsmenge M__ und der __Situation S__ zusammen (Klahold, 2009). Die folgende Abbildung zeigt die Funktionsweise eines Empfehlungssystems auf.

Das Benutzerprofil _P_ beinhaltet sowohl _explizite_ Informationen, wie z.B. Geschlecht oder Alter, als auch _implizite_ Informationen, wie z.B. gelesene Texte oder gekaufte Produkte. Die Entitätsmenge _M_ enthält die Elemente, die empfohlen werden können. Dies können beispielhaft Bücher oder Reisen sein. „Die Situation _S_ konstituiert sich aus Rahmenparametern der realen Welt (Datum, Uhrzeit, Geoinformation, verwendetes Endgerät des Benutzers, gerade angezeigter Text im Browser des Benutzers etc.)“ (Klahold, 2009, S.1). Aus der Entitätsmenge _M_ wird eine Teilmenge von Elementen _T_ gebildet, welche dem Nutzer empfohlen werden und die den Nutzen des Benutzers _B_ im gegebenen Kontext K maximieren sollen. Ziel des Empfehlungssystems ist es, die folgende Formel zu optimieren (Klahold, 2009):

max(Nutzwert(B,K,T)) mit K = (P,M,S)

Anders formuliert liegt das Ziel eines Recommender Systems darin, dem User individu-elle Inhalte, auch als Items bezeichnet, auf Basis seiner Bedürfnisse, Vorlieben und Inte-ressen zu empfehlen. Der Kunde soll auf für ihn relevante Produkt aufmerksam gemacht und zum Kauf angeregt werden (Höhfeld & Kwiatkowski, 2007).

## Techniken

Ein Recommender System kann mittels verschiedener Ansätze, welche in diesem Kapitel erläutert werden, realisiert werden. Zusätzlich werden die Vor- und Nachteile der jeweiligen Techniken aufgezeigt.

Die Ansätze setzten sich dabei aus dem inhaltsbasierten, kooperativen, demografischen, community-basierten und wissensbasierten Filtern sowie dem hybriden Verfahren zusammen.

### Inhaltsbasiertes Filtern

Das Verfahren „Information Retrieval”, bei dem es um das Bereitstellen von speziellen Informationen aus einer großen Menge von unsortierten Daten geht (Baeza-Yates & Ribeiro-Neto, 2011), bildet die Grundlage für das inhaltsbasierte Filtern (Balabanović & Shoham, 1997). 

Das inhaltsbasierte Filtern, auch _„content-based filtering“_ genannt, bezieht sich auf die Objekt-zu-Objekt-Korrelation und versucht auf Basis von Objekten, welche dem Nutzer in der Vergangenheit gefallen haben oder welche er gekauft hat, ähnliche Objekte zu finden und diese dem Benutzer anschließend zu empfehlen (Burke, 2007). 

Als Quelle für die Empfehlungsgenerierung werden Artikel- und Benutzerbeschreibungen herangezogen. Die Benutzerbeschreibungen beinhalten die Präferenzen und Interessen des Nutzers (Gemmis, Lops, Musto, Narducci & Semeraro, 2015), welche z.B. durch Ratings oder Kaufverhalten ausgedrückt werden können (Aggarwal, 2016), während die Artikelbeschreibungen die Merkmale des Produktes enthalten.

Zur Erstellung einer Empfehlung werden beide Beschreibungen miteinander abgeglichen und die Relevanz eines Produktes für den Kunden wird berechnet (Gemmis et al., 2015). 

Zur Bestimmung der Ähnlichkeit können verschiedene Distanzmaße herangezogen werden, wie z.B. das Cosinus-Ähnlichkeitsmaß (Cosine Similarity), der Pearson Korrelationskoeffizient, der Jaccard-Koeffizient, der euklidische Abstand oder das Nearest Neighbours-Verfahren (Klahold, 2009). 

Ein Beispiel für Empfehlungssysteme, welche auf Basis des inhaltsbasierten Ansatzes arbeiten, sind Systeme, die Nachrichtenartikel empfehlen, indem sie Schlüsselwörter aus einem Artikel, welcher der Kunde zuvor bewertet hat, mit den Schlüsselwörtern anderer Artikel vergleichen respektive abgleichen (Gärtner, 2012).

Ein Vorteil der inhaltsbasierten Empfehlungstechnik ist, dass sie vollkommen unabhängig von anderen Nutzern ist und die Empfehlung nur auf Basis der eigenen Interessen generiert wird. Des Weiteren ist die transparente Arbeitsweise ein Vorteil, da durch den Abgleich der Benutzer- und Produktbeschreibungen aufgezeigt werden kann, warum der jeweilige Artikel empfohlen wird. Dies führt dazu, dass das Vertrauen gegenüber dem Anwender erhöht werden kann. Ein weiterer Vorteil dieser Technik ist, dass dem Kunden auch neue Objekte empfohlen werden können, da die notwendigen Informationen aus der Produktbeschreibung herangezogen werden (Gärtner, 2012).

Den Vorteilen stehen jedoch auch Nachteile gegenüber. So können neue Objekte nur empfohlen werden, wenn sie bereits ausreichend beschrieben wurden. Diese Problematik betrifft vor allem komplexe Objekte wie z.B. Bilder.

Anders als neue Objekte, stellen vor allem neue Nutzer die Technik vor Probleme, dabei wird auch vom _„Kaltstartproblem“_ gesprochen. Sind nicht ausreichend Informationen über den Benutzer oder das Objekt vorhanden, z.B. da der Nutzer oder das Produkt neu ist, so wird entweder keine Empfehlung generiert oder eine sehr ungenaue. 

Das Kaltstartproblem bezieht sich sowohl auf neue Benutzer als auch auf neue Objekte. Für das inhaltsbasierte Filtern stellen allerdings, wie bereits erwähnt, nur neue Kunden ein Problem dar, da für die Erstellung einer Empfehlung die Nutzerdaten essenziell sind (Burke, 2007). Sind diese bei neuen Kunden nicht vorhanden, so gestaltet sich die Suche nach ähnlichen Produkten sehr schwierig. 

Eine weitere Problematik stellt das _„Serendipity-Problem“_, auch bekannt als Glücks- oder Zufallsproblem, dar. Darunter zu verstehen ist, dass dem Anwender keine unerwarteten Objekte aufgezeigt werden, sondern nur Objekte basierend auf dem vorhandenen Wissen (Gärtner, 2012).

Neben den vorgestellten Nachteilen stellt das _„Stability-vs-Plasticity“-Problem_ einen weiteren Nachteil dar, bei dem es darum geht, dass das Benutzerprofil, welches zu Beginn erstellt wird im Nachhinein nur schwer veränderbar ist (Burke, 2002). Burke (2002) beschreibt das Ganze anhand eines Beispiels wie folgt: „A steak-eater who becomes a vegetarian will continue to get steakhouse recommendations from a content-based or collaborative recommender for some time, until newer ratings have the chance to tip the scales” (Burke, 2002, S.338f).

### Kollaboratives Filtern

Das kollaborative Filtern, im Englischen als _„collaborative filtering“_ bezeichnet, ist der bekannteste, am weitesten verbreitete und ausgereifteste Ansatz (Burke, 2002).

Anders als beim inhaltsbasierten Filtern werden keine Korrelationen zwischen den Objekten gesucht, sondern zwischen den Nutzern, weshalb dabei auch von der „Mensch-zu-Mensch-Korrelation“ gesprochen wird (Burke, 2007).

Anstatt Artikel zu empfehlen, weil sie dem Benutzer in der Vergangenheit gefallen haben, werden Artikel empfohlen, die ähnlichen Nutzern gefallen haben. Dafür wird nicht wie bei dem inhaltsbasierten Filtern die Ähnlichkeit zwischen Produkten berechnet, sondern die Ähnlichkeit zwischen Benutzer (Balabanović & Shoham, 1997).

 Um die Ähnlichkeit zwischen Nutzern berechnen zu können, werden die einzelnen Interessen der Nutzer in Profilen gespeichert. Das Interesse der Nutzer an einem Produkt wird anhand der Produktbewertung repräsentiert (Pazzani, 1999). Die Produktbewertung kann über verschiedene Wege erfolgen, wie z.B. numerisch über eine Skala, die sich über eine beliebige Größe erstreckt oder binär, indem die Bewertung entweder positiv (z.B. „mag ich“) oder negativ (z.B. „mag ich nicht“) ist (Aggarwal, 2016). Die nachfolgende Abbildung 6 veranschaulicht die Funktionsweise des kollaborativen Filterns.

Der Ansatz des kollaborativen Filterns kann über zwei Wege realisiert werden. Zum einen über das _Memory-based collaborative Filtering_ und zum anderen über das _Model-based collaborative Filtering_ (Aggarwal, 2016).

_Memory-based collaborative Filtering_

Ersteres basiert darauf, dass Nutzer, die ein ähnliches Interesse haben, Items annähernd identisch bewerten werden. Mit dieser Annahme können anschließend Interessen bestimmt und Items dem entsprechenden Nutzer empfohlen werden. Zur Bestimmung der Nachbarschaft zwischen den Bewertungen können zwei Methoden angewendet werden.

Die erste Methode ist der _User-based_ Ansatz, bei dem der Nutzer im Mittelpunkt steht. Dabei wird davon ausgegangen, dass ähnliche Nutzer vergleichbare Bewertungen abgeben. 

Der zweite Ansatz ist die Item-based Methode, bei der anders als bei der User-based Methode das Produkt im Mittelpunkt steht. Hierbei werden die Ratings eines Kunden genutzt, um Ähnlichkeiten zwischen den Produkten, die der Nutzer in der Vergangenheit bewertet hat, zu bestimmen und anschließend ähnliche Produkte zu empfehlen. Gefallen beispielsweise zwei Produkte denselben Nutzern, so wird davon ausgegangen, dass sie sich ähnlich sind. 

Für die Berechnung werden kosinus- oder korrelationsbasierte Ähnlichkeitsmaße verwendet, die direkt auf die zur Verfügung stehenden Daten angewendet werden (Höhfeld & Kwiatkowski, 2007).

_Model-based collaborative Filtering_

Das Model-based collaborative Filtering verwendet Data Mining und Machine Learning Modelle, um Vorhersagen zu treffen (Aggarwal, 2016). „Bei der modellbasierten Variante hingegen wird offline ein Modell gelernt, auf das dann online zurückgegriffen werden kann. Es muss nicht mehr die komplette Datenmatrix aufgerufen werden. Bei dieser Form werden u.a. Techniken, wie die Neuronalen Netzwerke, die Latente Semantische Analyse, die Clusteranalyse oder die Bayesschen Netzwerke eingesetzt“ (Höhfeld & Kwiatkowski, 2007, S.267).

Vorteile des collaborative Filtering sind zum einen, dass kein branchenspezifisches Wissen benötigt wird, da die Empfehlung auf Basis ähnlicher Benutzerprofile generiert wird und nicht aus den Eigenschaften der Objekte.

Zum anderen werden keine expliziten Daten benötigt, da das System implizite Daten aus der Nutzerbeobachtung gewinnt (Burke, 2007). Des Weiteren liefert das kollaborative Filtern den Vorteil, dass die Technik Empfehlungen auch „outside the box“ generiert, d.h. dem Anwender werden neue Objekte aufgezeigt, auf die er eventuell nicht von selbst aufmerksam geworden wäre. 

Durch den Einsatz von Machine Learning Algorithmen hat der Ansatz des kollaborativen Filterns den Vorteil, dass das ganze System lernfähig ist und mit voranschreitender Zeit die Qualität der Empfehlung verbessern kann (Burke, 2002).

Wie beim inhaltsbasierten Ansatz stellt das _Kaltstartproblem_ auch beim kollaborativen Ansatz ein wesentliches Problem dar. Jedoch stellen in diesem Fall sowohl neue Nutzer als auch neue Objekte die Technik vor Probleme.

Auf der einen Seite werden für die Generierung Bewertungen für neue Objekte benötigt und auf der anderen Seite Informationen über den Benutzer, um Ähnlichkeiten zu anderen Nutzern zu ermitteln. Diese Informationen sind zu Beginn des Systems nicht vorhanden und deshalb können keine Ähnlichkeiten berechnet werden. 

Neben dem Kaltstartproblem stellt das _„Grey-Sheep“-Problem_ eine weitere Problematik dar. Unter den ‚grauen Schafen‘ sind Nutzer zu verstehen die nicht genau in eine Benutzergruppe fallen, sondern sich zwischen verschiedenen Benutzergruppen bewegen (Burke, 2002).

Ebenso trifft auch das _„Stability-vs-Plasticity“-Problem_ bei diesem Ansatz zu. Um kollaborative Empfehlungssysteme effizient nutzen zu können, wird eine angemessene Anzahl von Daten benötigt. Diese darf einerseits nicht zu klein sein, da sonst keine Empfehlungen generiert werden können, aber anderseits auch nicht zu groß, da ansonsten sowohl die Memory-based- als auch die Model-based-Methode an ihre Grenzen stoßen (Gärtner, 2012).
