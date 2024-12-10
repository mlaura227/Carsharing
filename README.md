# Mészáros Laura - Szakdolgozat
## Közösségi autómegosztó szolgáltatók összehasonlítása felhasználói vélemények alapján, mélytanuló szövegelemző modellekkel
Kutatásomban a három hazai közösségi autómegosztó szolgáltatót hasonlítom össze, az applikációikra kapott értékelések alapján. Ezeket data scraping megoldással gyűjtöttem össze a magyar Google Play Áruház és App Store platformokról. A kutatásom célja, hogy meghatározzam, összességében vajon kiemelkedik-e egy szolgáltató a három közül. Ezen állítás vizsgálatát különböző, szövegelemző és mélytanuló modellek segítségével végeztem el.

Az adatállományt önmagában is feldolgoztam, illetve számos adatbővítő módszerek használatával is, mint a SMOTE vagy a visszafordítás, a minél optimálisabb eredmények biztosításához. LDA modell alkalmazásával elemeztem az azonosítható témákat, az értékelések összetettebb megismerése érdekében. Valamint a BERT transzformátor alapú, nagy nyelvi modell több variációjával végeztem szentiment analízist. Többek között felhasználtam a DistilBERT, XLM-RoBERTa, huBERT modelleket az algoritmusok felépítésére, de LSTM 
modellek architektúráival is kísérleteztem. Ezen modellek teljesítményének mérésére olyan többosztályos klasszifikációra alkalmas metrikákat alkalmaztam, mint az accuracy, precision, recall, F1-score, illetve a ROC-görbe mutatók. A kutatásban kiemelt szerepet kaptak a modellek finomhangolási folyamatai, amelyek célja az osztályozási pontosság javítása volt. A metrikák 
alapján legjobb teljesítményt nyújtó transzformátor modell variánsának finomhangolt verzióját beágyazó modellként implementáltam egy, a LangChain keretrendszer eszközével, RAG modell kialakításához. A modellt többféleképpen igyekeztem optimalizálni, először az adathalmazának módosításával. Megnéztem, hogyan működik az eredeti állományon, illetve az 
optimális transzformátor egy prediktált állományán a szolgáltatók gyakran ismételt kérdéseinek dokumentumával kiegészítve, továbbá csupán az eredeti halmazt felhasználva is. Utóbbi megoldás biztosított stabil működést a visszakereséssel továbbfejlesztett klasszifikáción. Az így kapott modell különböző lekérdezésekre és kérdések megválaszolására szolgált, beleértve egyes kutatási kérdéseket is.
