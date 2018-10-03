# AlgDat-tdt4120

## Forelesningsplan
---

**Læringsmål for hver algoritme**:
- Kjenne den formelle definisjonen av det generelle problemet den løser
- Kjenne til eventuelle tilleggskrav den stiller for å være korrekt
- Vite hvordan den oppfører seg; kunne utføre algoritmen, trinn for trinn
- **Forstå korrekthetsbeviset; hvordan og hvorfor virker algoritmen egentlig?**
- Kjenne til eventuelle styrker eller svakheter, sammenlignet med andre
- Kjenne kjøretidene under ulike omstendigheter, og forstå utregningen

## Forelesning 1

Vi starter med fagfeltets grunnleggende byggesteiner, og skisserer et rammeverk for å tilegne seg resten av sto et. Spesielt viktig er ideen bak induksjon og rekursjon: Vi trenger bare se på siste trinn, og kan anta at resten er på plass.

### Pensum: 
- [ ] Kap. 1. The role of algorithms in computing
- [ ] Kap. 2. Getting started: Innledning, 2.1–2.2
- [ ] Kap. 3. Growth of functions: Innledning og 3.1

### Læringsmål:
- [x] Forstå bokas pseudokode-konvensjoner
- [x] Kjenne egenskapene til random-access machine-modellen (RAM)
- [x] Kunne definere problem, instans og problemstørrelse
- [x] **Kunne definere asymptotisk notasjon, O, Ω , Θ , o og ω.**
- [x] **Kunne definere best-case, average-case og worst-case**
- [ ] **Forstå løkkeinvarianter og induksjon**
- [ ] **Forstå rekursiv dekomponering og induksjon over delproblemer**
- [x] Forstå Insertion-Sort

## Notater

**Algorithm**: a well-defined computational procedure that takes some value, or set of values as *input* and produces some value, or set of values, as *output*.

**Computational problem**: algoritms are a tool for solving these problems. The statement of the problem specifies in general terms the desired input/output relationship.

**Instance**: an input sequence in the form of -> (26, 31, 41, 41, 58, 59).

**Data structure**: The book contains several data structures. It is a way to store andd organize data in order to facilitate access and modifications. No single data structure works well for all purposes.

**Problem**: relation between input and output

**Problem-size**: memory needed for an instance

**NP-completet**: no effective algorithms exist for these problems. They arise surprisingly often in real applications. If you can show that a problem is NP-complete, you can spend toy developing an efficient algorithm that fives a good, but not the best possible solution.

*We should consider algorithms, like computer hardware, as a technology. Total system performance depends on choosing efficeint alghorithms as much as on choosing fast hardware.*

**Random-access machine (RAM)**: we must have a model for the resorces of that technology and their costs. Our RAM model executes instructions one after another. The RAM model contains instructions such as add, subtract, multiplu, divide, remainder, floor, ceiling. Each insctruction takes a constant amount of time.

**Insertion sort**

- Solves a sorting problem. The numbers we wish to sort are called **keys**. It is effective for a small number of elements
- If we have an empty hand and all the cards on the table faced down. We remove one card at a time fram the table and insert it into the correct position in the left hand. To find the correct position for a card, we compare it with each of the cards already in the hand, from right to left.

    
       INSERTION-SORT(A)
       1 for j = 2 to A.length
       2    key = A[j]
       3    //insert A[j] into the sorted sewuence A[1..j-1]
       4    while i > 0 and A[1] > key
       5        A[i+1] = A[i]
       6        i = i-1
       7    A[i+1] = key

- Best case: occurs if the array is already sorted. This is them a linear finction (**Θ(n)**)
- Worst case: occurs if the array is reverse sorted. It is a quadratic function of n (**Θ(n<sup>**2**</sup>)**)


**Asymptotic notation**

Asymptotic efficiency is when we look at input sizes large enough to make only the order of grwth of the running time relevant.
- **Θ-notation**: bounds a function within two constant factors
- **O-notation**: gives an upper bound for a function to within a constant factor
- **Ω-notation**: gives a lower bound for a function to within a constant factor

Rule of thumb
     <pre>
      ω > Θ(f(n)) (Small Omega)
      Ω ≧ Θ(f(n)) (Big Omega)
      Θ = Θ(f(n)) (Big Theta)
      O ≦ Θ(f(n)) (Big O)
      o < Θ(f(n)) (Small o)
      </pre>
