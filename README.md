# Summary

The UD Tamil treebank is based on the Tamil Dependency Treebank created at the
Charles University in Prague by Loganathan Ramasamy.


# Introduction

The treebank was part of
HamleDT, a collection of treebanks converted to the Prague dependency style
(since 2011). Later versions of HamleDT added a conversion to the Stanford
dependencies (2014) and to Universal Dependencies (HamleDT 3.0, 2015). The
first release of Universal Dependencies that includes this treebank is UD v1.2
in November 2015. It is essentially the HamleDT conversion but the data is not
identical to HamleDT 3.0 because the conversion procedure has been further
improved.

## References:

* [TamilTB](http://ufal.mff.cuni.cz/~ramasamy/tamiltb/0.1/)
* [HamleDT](http://ufal.mff.cuni.cz/hamledt)
* [Treex](http://ufal.mff.cuni.cz/treex) is the software used for conversion
* [Interset](http://ufal.mff.cuni.cz/interset) was used to convert POS tags and features
* Loganathan Ramasamy, Zdeněk Žabokrtský. 2012.
  [Prague Dependency Style Treebank for Tamil](http://www.lrec-conf.org/proceedings/lrec2012/summaries/456.html).
  In: *Proceedings of Eighth International Conference on Language Resources and Evaluation (LREC 2012),*
  İstanbul, Turkey, ISBN 978-2-9517408-7-7, pp. 1888–1894.

<pre>
@inproceedings{ta,
  author    = {Ramasamy, Loganathan and \v{Z}abokrtsk\'{y}, Zden\v{e}k},
  year      = {2012},
  title     = {Prague Dependency Style Treebank for {Tamil}},
  booktitle = {Proceedings of Eighth International Conference on Language Resources and Evaluation ({LREC} 2012)},
  address   = {\.{I}stanbul, Turkey},
  editor    = {Nicoletta Calzolari (Conference Chair) and Khalid Choukri and Thierry Declerck and Mehmet Uğur Doğan and Bente Maegaard and Joseph Mariani and Asuncion Moreno and Jan Odijk and Stelios Piperidis},
  isbn      = {978-2-9517408-7-7},
  pages     = {1888--1894},
  url       = {http://www.lrec-conf.org/proceedings/lrec2012/summaries/456.html}
}
</pre>


# Source of annotations

This table summarizes the origins and checking of the various columns of the CoNLL-U data.

| Column | Status |
| ------ | ------ |
| ID | Sentence segmentation and tokenization (including cutting off certain suffixes that constitute independent syntactic words) was automatically done and then hand-corrected. |
| FORM | Identical to TamilTB form. |
| LEMMA | Gold (preprocessed and then manually corrected). |
| UPOSTAG | Converted automatically from XPOSTAG (via [Interset](https://ufal.mff.cuni.cz/interset)). |
| XPOSTAG | Gold (preprocessed and then manually corrected). |
| FEATS | Converted automatically from XPOSTAG (via Interset). |
| HEAD | Original TamilTB annotation is manual (preprocessed by a rule-based parser and then manually corrected). Automatic conversion to UD; human checking of patterns revealed by automatic consistency tests. |
| DEPREL | Original TamilTB annotation is manual (preprocessed by a rule-based parser and then manually corrected). Automatic conversion to UD; human checking of patterns revealed by automatic consistency tests. |
| DEPS | &mdash; (currently unused) |
| MISC | Information about token spacing restored using heuristics. Mapping between multi-word tokens and syntactic words verified against the source text. |


# Changelog

* 2019-05-15 v2.4
  * Fixed some annotation errors in the original treebank, re-run the conversion.
  * Dative and instrumental objects are now treated as oblique arguments.
* 2018-04-15 v2.2
  * Repository renamed from UD_Tamil to UD_Tamil-TTB.
  * Added enhanced representation of dependencies propagated across coordination.
    The distinction of shared and private dependents is derived deterministically from the original Prague annotation.
* 2017-03-01 v2.0
  * Converted to UD v2 guidelines.
  * Reconsidered PRON vs. DET distinction.
  * Improved advmod vs. obl distinction.
* 2016-05-15 v1.3
  * Added Latin transliteration of lemmas and full sentences.
  * Added orthographic words (surface tokens) and their mapping to nodes.
  * Improved conversion of AuxY.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v1.2
License: CC BY-NC-SA 3.0
Includes text: yes
Genre: news
Lemmas: converted from manual
UPOS: converted from manual
XPOS: manual native
Features: converted from manual
Relations: converted from manual
Contributors: Ramasamy, Loganathan; Zeman, Daniel
Contributing: elsewhere
Contact: zeman@ufal.mff.cuni.cz
===============================================================================
</pre>
