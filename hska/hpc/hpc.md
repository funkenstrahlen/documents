Zusammenfassung _I W909 High Performance Computing_ WS 14/15
============================================================

# 1 Introduction

## Literatur

* [Parallele Programmierung](htt_{P}://link.springer.com/book/10.1007%2F978-3-642-13604-7)
* [The OpenCL Programming Book](htt_{P}://www.fixstars.com/en/opencl/book/)

## Wichtige Kennzahlen

### Speedup

| Variable | Bedeutung |
| ----- | ----- |
| $t_{S}$ | Sequentielle Laufzeit |
| $t_{P}$ | Parallele Laufzeit |
| $S$  | Speedup |

$S = \frac{t_{S}}{t_{P}}$


### Effizienz

| Variable | Bedeutung |
| ----- | ----- |
|$E$ | Effizienz |
|$P$ | Anzahl Prozessoren (optimaler Speedup) |

$E = \frac{S}{P}$

### Amdahl

| Variable | Bedeutung |
| ----- | ----- |
|$t_{S}$ | Anteil der sequentiell ausgeführt wird |
|$t_{P}$ | Anteil der parallel ausgeführt wird |
|$P$ | Anzahl Prozessoren (optimaler Speedup) |

$S = \frac{1}{t_{S} + \frac{t_{P}}{P}} = \frac{1}{(1 - t_{P}) + \frac{t_{P}}{P}}$

> Parallelisierung bringt keinen wesentlichen Speedup und ist nicht effizient.

### Gustafson

$S = t_{S} + P * t_{P}$

> Parallelisierung kann jeden Speedup und einen hohen Grad an Effizienz erreichen wenn das Problem groß genug ist und genug CPU genutzt wird.


## Speichermodelle

### Shared Memory

* Ein globaler Adressraum auf den alle Prozessoren zugreifen
* Änderungen im Speicher sind für alle Prozessoren sichtbar (uu. nicht sofort)


### Distributed Memory

* Zugriff auf Speicher von anderem Prozessor erfolgt über Netzwerk
* Jeder Prozessor hat eigenen Speicher
* Änderungen eines Prozessors sind nicht für andere sichtbar


### Vor- und Nachteile

| Shared Memory | Distributed Memory |
| ------------- | ------------------ |
| + Einfacher Datenaustausch | - Schwerer Datenaustausch (manueller Aufwand) |
| - Schwerer Datenzugriff (manueller Aufwand) | + Einfacher Datenzugriff |
| + Schnelle und einfache parallelisierung | - Kommunikation muss entworfen werden |
| - Beschränkte Skalierbarkeit | + (uU.) gute Skalierbarkeit |

### Hybride Programmierung

* Mischung aus Shared und Distributed
* Manueller Aufwand für Datenaustauch und Datenzugriff
* Kommunikation notwendig
* Dafür: Gute Skalierbarkeit


# 2 openMP



# 3 MPI



# 4 CPU



# 5 Performance



# 6 Errors



# 7 Networks



# 8 GPU / OpenCl



# 9 Patterns



