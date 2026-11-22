# Executive Summary

The full dataset contains 6,741,595 observations, 4,063,772 sessions, and 241 services. The configured role layer classifies 2 services as horizontal and 239 as domain services.

Full ecosystem: 211 communities, 7760 complete service pairs, and 4,063,772 sessions. Domain ecosystem: 221 communities, 7357 complete service pairs, and 3,530,536 sessions containing at least one domain service.

Horizontal services can distort ecosystem structure when they occur broadly across unrelated administrative journeys. Compare community_comparison.csv: an increase in community count and a reduction in largest-community size after removal are evidence that platform services were connecting otherwise distinct domains under this graph construction.

Meaningful administrative ecosystems that remain in the domain graph are represented by domain-only communities, their dominant themes, centrality rankings, and recurring journeys. These are more suitable as LLM planning targets than profile/inbox context services.

The revised CSJM adds an explicit role layer and paired full/domain layers, allowing recommendation and agent navigation systems to condition on user context separately from administrative intent. Centrality shifts and journey comparison expose domain hubs, bridge services, disappearing platform-mediated journeys, and newly emerging administrative bundles.

## Layer 2A and Layer 2B
Layer 2A preserves raw co-occurrence and support. Layer 2B normalizes each pair by the union of the two services' session populations using Jaccard similarity, surfacing focused behavioral relationships that raw popularity can hide.

### Relationships emerging after normalization
| service_a | service_b | cooccurrence_count | support | jaccard_similarity |
| --- | --- | --- | --- | --- |
| Korisnički pretinac | Moj profil | 763909 | 0.18798028 | 0.39248568 |
| Registar birača | e-Birači | 103 | 2.535e-05 | 0.33118971 |
| Moj profil | Portal zdravlja | 559678 | 0.13772377 | 0.29477961 |
| Porezna prijava za obračun i plaćanje posebnog poreza na motorna vozila | Registar proizvođača s proširenom odgovornosti (RPPO) | 5636 | 0.00138689 | 0.17115093 |
| Financijske kartice Grada Sveti Ivan Zelina | Otvoreni grad Ivanić Grad | 2 | 4.9e-07 | 0.15384615 |
| e-Matične knjige | e-Usluge MUP-a | 24118 | 0.00593488 | 0.14576245 |
| Financijske kartice Grad Dugo Selo i Sustav informiranja građana objavljeno na platformi OTVORENI GRAD DUGO SELO | Otvoreni grad Ivanić Grad | 2 | 4.9e-07 | 0.125 |
| Mirovinsko osiguravajuće društvo (prijava/promjena) | Odabir mirovine (mirovina samo iz I. stupa ili mirovina iz I. i II. stupa) | 292 | 7.185e-05 | 0.12274065 |
| Korisnički pretinac | Portal zdravlja | 192088 | 0.0472684 | 0.11449546 |
| Geoportal ISPU | ePlanovi editor | 589 | 0.00014494 | 0.10803375 |

The affinity graph contains 14 behavioral communities after isolated services are removed. These communities make service ecosystems clearer when broadly used platform services would otherwise dominate co-occurrence structure.

### Affinity-based hubs
| service | session_count | weighted_degree | betweenness_centrality | behavioral_hub_score |
| --- | --- | --- | --- | --- |
| Moj profil | 1649388 | 1.24536245 | 0.09612036147041168 | 1.36506714 |
| Korisnički pretinac | 1060857 | 1.12626394 | 0.09409518871307868 | 1.23223996 |
| e-Usluge MUP-a | 87191 | 0.71312895 | 0.01996946838803301 | 0.72736976 |
| e-Matične knjige | 102388 | 0.68736311 | 0.01592165664515548 | 0.69830707 |
| Portal zdravlja | 808922 | 0.6322137 | 0.039140830877580926 | 0.65695907 |
| e-Usluge HZMO-a | 152983 | 0.4858002 | 0.01292337149861553 | 0.49207838 |
| Moj OIB | 33236 | 0.47882354 | 0.011581871120859672 | 0.48436921 |
| e-Birači | 271 | 0.4500082 | 0.00035719471533105824 | 0.45016894 |
| Moja mirovina | 43404 | 0.43380936 | 0.01594143780963514 | 0.4407249 |
| Registar birača | 143 | 0.42656262 | 0.0003387961628897509 | 0.42670714 |

The affinity layer strengthens CSJM by separating frequency from relationship strength. Its normalized pairs, behavioral communities, local affinity subgraphs, and hub rankings can later support service recommendation, benchmark generation, and intelligent agent planning.