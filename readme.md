# BLIZZWORD V1.0  [![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
 
## A free resource for linguistic game studies

### Authors
Jérôme Jacquin & Aris Xanthos  
Department of Language and Information Sciences  
University of Lausanne

### Synopsis
BLIZZWORD is a corpus of rule and flavor text from Hearthstone&reg; cards. Card texts were originally retrieved from the [HearthstoneJSON website](https://hearthstonejson.com/), then converted to XML, tokenized, lemmatized and POS-tagged by the authors as part of an academic research project in the field of linguistic game studies.

In the hope of fostering research in this emerging field, the BLIZZWORD corpus is released publicly and licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

### Documentation
Blizzword contains all Hearthstone cards published between the game's public release in August 2013 and December 2015 (i.e. shortly before the developer introduced the "standard" mode and started removig cards from the game). This corresponds to the following card sets, in addition to a dozen special cards (hero skins, rewards, promotions): 

| Code      | Name                 | Release           | Type      | # Cards |
|-----------|----------------------|-------------------|-----------|---------|
| BAS       | Basic                | March 11, 2014    | Core      | 133     |
| CLA       | Classic              | March 11, 2014    | Core      | 245     |
| NAX       | Curse of Naxxramas   | July 22, 2014     | Adventure | 30      |
| GVG       | Goblins and Gnomes   | December 8, 2014  | Expansion | 123     |
| BRM       | Blackrock Mountain   | April 2, 2015     | Adventure | 31      |
| TGT       | The Grand Tournament | August 24, 2015   | Expansion | 132     |
| LOE       | League of Explorers  | November 12, 2015 | Adventure | 45      |
| **TOTAL** |                      |                   |           | **739** |

Each card is enclosed in a `<card>` tag with a number of attributes (see example below). It usually contains a `<rules>` tag, which contains the text describing the card's effect, and a `<flavor>` tag which contains the so-called "flavor text", used to relate the card with the game’s cultural background. These texts are then further divided into `<token>` tags, each of which has a `lemma` and `pos-tag` attribute. Here's an example of a card in BLIZZWORD:
```xml
  <card name="Fallen Hero" num="468" id="AT_003" set="6_TGT" cost="2" attack="3" health="2" rarity="RARE" category="MINION" playerClass="MAGE">
    <rules>
      <token lemma="your" pos-tag="det|poss">Your</token>
      <token lemma="Hero Power" pos-tag="n|sg">Hero Power</token>
      <token lemma="deal|v" pos-tag="v|ind_pres">deals</token>
      <token lemma="1" pos-tag="num">1</token>
      <token lemma="extra|adj" pos-tag="adj">extra</token>
      <token lemma="damage|n" pos-tag="n|sg">damage</token>
      <token lemma="." pos-tag="pun|period">.</token>
    </rules>
    <flavor>
      <token lemma="and" pos-tag="conj|coord">And</token>
      <token lemma="he" pos-tag="pro|subj">he</token>
      <token lemma="can|vmod" pos-tag="vmod|ind_pres">can</token>
      <token lemma="not" pos-tag="adv|neg">'t</token>
      <token lemma="get|v" pos-tag="v|inf">get</token>
      <token lemma="up" pos-tag="adv">up</token>
      <token lemma="." pos-tag="pun|period">.</token>
    </flavor>
  </card>

```
### Acknowledgements
The authors are most grateful to the Faculty of Arts of the University of Lausanne for the financial support and to Laura Schött for her participation in the corpus annotation.

### Outcomes
- Jacquin, J., & Xanthos, A. (2017). Approche de l’évolution de la complexité linguistique dans un jeu de cartes numérique: L’exemple d’Hearthstone. Colloque international « Penser (avec) la culture vidéoludique », Lausanne (Switzerland).
- Jacquin, J., & Xanthos, A. (2019). L’évolution de la complexité linguistique dans un jeu de cartes numérique: Un exemple de Linguistic Game Studies. Colloque international « Les langages du jeu vidéo : codes, discours et images en jeu », Lausanne (Switzerland). https://www.youtube.com/watch?v=FUXLIqXegUM
- Jacquin, J., & Xanthos, A. (2021). Evolution of linguistic complexity in Hearthstone: A resource and an example in linguistic game studies. Digital Scholarship in the Humanities, 36(4), 907–918. https://doi.org/10.1093/llc/fqaa065
