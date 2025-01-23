# rcis2025

This is the online repository for the article "Modelling Hierarchies of Organisational Rules", RCIS 2025

The Wikibase cloud instantiation is available at: https://rule-hierarchies.wikibase.cloud/

The Kumu mas is available at: https://kumu.io/joran/rule-hierarchies-v3-dynamic

This is the SPARQL query: 

PREFIX wd: <https://rule-hierarchies.wikibase.cloud/entity/>
PREFIX wdt: <https://rule-hierarchies.wikibase.cloud/prop/direct/>
PREFIX wikibase: <http://wikiba.se/ontology#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX bd: <http://www.bigdata.com/rdf#>

SELECT ?item ?itemLabel 
       ?instanceof ?instanceofLabel 
       ?subclassof ?subclassofLabel 
       ?hasscope ?hasscopeLabel 
       ?hasterritorialscope ?hasterritorialscopeLabel 
       ?hasruletype ?hasruletypeLabel 
       ?partofcomposition ?partofcompositionLabel 
       ?cites ?citesLabel 
       ?repeals ?repealsLabel 
       ?subpropertyof ?subpropertyofLabel 
       ?partofaggregation ?partofaggregationLabel 
       ?delegatesto ?delegatestoLabel 
       ?complieswith ?complieswithLabel 
       ?subordinateto ?subordinatetoLabel 
       ?hascompliancecitationfrom ?hascompliancecitationfromLabel 
       ?haspartaggregation ?haspartaggregationLabel 
       ?haspartcomposition ?haspartcompositionLabel 
       ?citedby ?citedbyLabel 
       ?hascompliancecitationfromrecursivenumber ?hascompliancecitationfromrecursivenumberLabel 
       ?haspartaggragationrecursivenumber ?haspartaggragationrecursivenumberLabel 
       ?superiorto ?superiortoLabel 
       ?superiortorecursivenumber ?superiortorecursivenumberLabel
       ?hasmaterialscope ?hasmaterialscopeLabel
       ?haspartcompositionrecursivenumber ?haspartcompositionrecursivenumberLabel
       ?haspartrecursivenumber ?haspartrecursivenumberLabel
       ?hasscoperecursivenumber ?hasscoperecursivenumberLabel
       ?hasterritorialscoperecursivenumber ?hasterritorialscoperecursivenumberLabel

WHERE
{
  OPTIONAL {?item wdt:P1 ?instanceof.} # Must be a cat
  OPTIONAL {?item wdt:P2 ?subclassof.}
  OPTIONAL {?item wdt:P3 ?hasscope.}
  OPTIONAL {?item wdt:P4 ?hasterritorialscope.}
  OPTIONAL {?item wdt:P5 ?hasruletype.}
  OPTIONAL {?item wdt:P6 ?partofcomposition.}
OPTIONAL {?item wdt:P7 ?cites.}
OPTIONAL {?item wdt:P8 ?repeals.}
OPTIONAL {?item wdt:P9 ?subpropertyof.}
OPTIONAL {?item wdt:P10 ?partofaggregation.}
OPTIONAL {?item wdt:P11 ?delegatesto.}
OPTIONAL {?item wdt:P12 ?complieswith.}
OPTIONAL {?item wdt:P13 ?subordinateto.}
OPTIONAL {?item wdt:P14 ?hascompliancecitationfrom.}
OPTIONAL {?item wdt:P15 ?haspartaggregation.}
OPTIONAL {?item wdt:P16 ?haspartcomposition.}
OPTIONAL {?item wdt:P17 ?citedby.}
OPTIONAL {?item wdt:P18 ?hascompliancecitationfromrecursivenumber.}
OPTIONAL {?item wdt:P19 ?haspartaggragationrecursivenumber.}
OPTIONAL {?item wdt:P20 ?superiorto.}
OPTIONAL {?item wdt:P21 ?superiortorecursivenumber.}
OPTIONAL {?item wdt:P22 ?hasmaterialscope.}
OPTIONAL {?item wdt:P23 ?haspartcompositionrecursivenumber.}
OPTIONAL {?item wdt:P24 ?haspartrecursivenumber.}
OPTIONAL {?item wdt:P25 ?hasscoperecursivenumber.}
OPTIONAL {?item wdt:P26 ?hasterritorialscoperecursivenumber.}
  SERVICE wikibase:label { 
    bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". 
  }
}
