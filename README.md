CEPI-BASE: p.213 Excercici Cartellera jQuery
============================================
Arxius utilitzats:

Caratulasjquery
    index.html
    ejson1.json (una versió modificada del mateix del TEMA7_AJAX)
    
-------------------------------------------------------------------
NOTES I PENSAMENTS PER AL DESENVOLUPAMENT DE L'EXCERCICI:

-[RESOLT] quins llenguatges utilitzem per recollir l'informació?
    - Les dades del formulari es recullen en un PHP
    - jQuery s’escriu en Javascript

HTML/FORMULARI->PHP->JAVASCRIPT->HTML/ID=CONTENIDO

També podem recollir informació directament d’un formulari amb Javascript?
si, amb jQuery el que fem es recollir els events de formulari

A l’exemple dels apunts recull el click i passa la funció que desenvolupa el JSON
______________________________________________________________________________________________________

-[RESOLT] Repassar que és cada cosa del JSON, per saber com treure el “discos” que suggereix l’exemple
		- Literals d’objecte “Nombre”:”Margarita”.
		Això crea un objete que disposará de dues propietats anomenades nom i valor:

Var cos =	{“nom”:”a”,
		     “valor”:”b”,
		    }

		Podem accedir a elles utilitzant la notació d’objectes, amb un punt, seguida de la propietat:
        cos.nom;
		cos.valor;

Literals mixtos:
================
(es barregen literals d’objecte i arrays,
creant d’aquesta forma un array d’objectes o un objecte que contingui un array)

Nomenclatura:

{ } -> objecte
[ ] -> array
"_":"_" -> propietat

Llavors el fitxer ejson1.json estaria compost per:
(objecte dins d'un array per fora [] i per dins {})

   discos -> Propietat : valor dels discos->Array
                            aquest Array conté diversos objectes:
                                Aquests objectes contenen varies propietats.
___________________________________________________________________________
 -[RESOLT] com expressem l'envent pels inputs de radio?
 
 Hi ha un tipus de selector :radio
 
 :radio  The <input>  elements with type="radio" .

es posa així:
$(:radio)

Per un set d'elements radio es posaria:

$( "input[name=gender]:radio" )

usem el .change() no el .on("click"), doncs aquest primer es més específic per a radio buttons

https://api.jquery.com/change/
______________________________________________________________________________________________

-[PENDENT] ara he aconseguit de que surtin tots, i necessito que només surtin els de cada botó
