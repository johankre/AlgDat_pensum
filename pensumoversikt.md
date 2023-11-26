# Algoritmer og Datastrukturer

## Forelesning 1. Problemer og Algoritmer
Vi starter med fagfeltets grunnleggende byggesteiner, og skisserer et rammeverk for å tilegne seg resten av stoffet.
Spesielt viktig er ideen bak induksjon og rekursjon:
Vi trenger bare se på site trinn, og kan anta at resten er på plass.

### $A_1$ Forstå bokas *pseudokode*-konvensjoner
- Dette er trivielt

### $A_2$ Kjenne egenskapene til *random-access machine*-moddellen (RAM)
- I RAM modellen blir instruksjoner kjørt sekvensielt. 
Det betyr instruksjonene kjøres en etter en, i tillegg til at ingen instruksjoner kjøres samtidlig.

- RAM antar at alle instruksjoner tar like lang tid, samt aksesering av data.
Det betyr at modellen antar at instruksjoner eller aksesering av data tar konstant tid.

- RAM har dermed begrensninger ved analyse av algoritmer.
Likevel er RAM-modellen ofte et godt midel for analyse av ytelse på faktiske maskiner. 

- RAM modellen tar ikke høyde for mine hierarki.
Mine-hierarki kan ha en stor innflyttelse på programmet sin faktiske kjøretid. 

### $A_3$ Kunne definer problem, instans og problemstørrelse.
- **Problem**: er en generell relasjon mellom input og output.
- **Instans**: en konkret input.
- **Problemstørrelsen, n**: Lagringsplass som trengs for en instans.  
Kan variere med hvordan vi måler størrelse.

### $A_4$ Kunne definere og bruke asymptotisk notasjon $O,\Omega, \Theta, o$ og $\omega$.
- Asymptotisk notasjon beskriver effektiviteten til en algoritme når input størrelsen er stor nokk til at kunn vekstfaktoren av kjøretid er relevant.  
Tenk

        O(n) vs O(n!)
    ikke

        O(an) vs O(bn!)
    $\rightarrow$ ser ikk på konstantene $a,b$.

- Generelt er en algoritme som er asymptotisk mer effektiv, et bedre valg for alle input størrelser, bortset fra noen få tilfeller.

- **$O$-notation**  
    Brukes til å angi øvre grense.  
    Formel definisjon:

        O(g(n)) = {f(n): there exsist a positive constant c and n_0 s.t. 
                    0 <= f(n) <= cg(n) for all n >= n_0}
    Eksempel:  
    Figuren viser at $n²$ er en øvre grense for funksjonen $O(n²)$, om  vi skalerer grensen som vi vil, og velger en høy nokk n.
    ![alt text](/home/johannes/NTNU/2023H/AlgDat/pensum_img/o_n.png)
    Den sentrale egenskapen er at $O(n²)$ ligger under $cn²$ for store verdier av $n$.

- $\Theta$ - notation  
Brukes til å angi at funksjonen er bunnet, altså har samme vekstfaktor for øvre og nedre grense, men med ulike skalerings faktorer.   
Eksempel: $n²$
    ![alt text](/home/johannes/NTNU/2023H/AlgDat/pensum_img/theta_n.png)  
    Sentralt er at $\Theta (n²)$ ligger mellom $c_2n²$ og $c_1n²$ for store $n$.  
    En anne måte å formulere det på er at funksjonen likker mellom to skaleringer av samme kurve.

- $\Omega$- notation  
$\Omega$ brukes for å angi nedre grense for store $n$.  
Eksempel: $n²$  
    ![alt text](/home/johannes/NTNU/2023H/AlgDat/pensum_img/omega_n.png)

- Eksempel på bruk av ssymptotisk notasjon  
$O(n^a) + \Omega (n^b) + \Theta(n^c) = \Omega (n^b + n^c)$  
$n² + O(n) = O(n²)$



