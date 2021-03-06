Following a suggestion by Avram, I had a deeper look into Marc.js and 
the possibilities of enhancing MARC support in Zotero. This concerns UNIMARC 
in particular, but I am trying to address Marc-21, too. There is nothing 
to be gained and much to be lost by hurrying things in such a central place 
as the MARC engine is - this is just meant as a starting point.

Follwing just another one of Avram's suggestions, I am trying to
explore [Frank Benett's multilingual Zotero extensions](http://gsl-nagoya-u.net/http/pub/zotero-multilingual-overview.html) and their
possible integration with MARC.

Project contents
----------------

* An importer [Marc2.js](http://github.com/zomark/zotero-marc/blob/master/MARC2.js), 
capable of importing binary Unimarc- and
Marc-21 files. My import tests have been very limited, though.
Marc2.js also exposes a "Marc" namespace which is the entry point for
translators using the module. This namespace attempts to model MARC
records with leaders, field and subfields, exposes a number of handy
constants and helper classes that clients can use to convert between
Zotero items, MARC records and external MARC representations (textual
or binary).

* the JSDoc-generated [docs](http://github.com/zomark/zotero-marc/tree/master/doc/) for Marc2.js (obviously insufficient)

* two translators using Marc2.js. The examples intends to demonstrate how Marc translators 
could become a little cleaner and maybe easier to maintain:
- [Library Catalog (Dynix)2.js](http://github.com/zomark/zotero-marc/blob/master/Library%20Catalog%20(Dynix)2.js) 
	(test [here]http://www.babord.univ-bordeaux.fr))
- [Catalog Collectif de France.js](http://github.com/zomark/zotero-marc/blob/master/Catalogue%20Collectif%20de%20France.js) 
	(test [here](http://www.ccfr.bnf.fr))

* [sample data](http://github.com/zomark/zotero-marc/tree/master/sampledata/) in binary MARC format

* some proposed [patches](http://github.com/zomark/zotero-marc/tree/master/sampledata/) concerning the multilingual features

There is nothing revolutionary in this, and the current MARC support
works fine, thanks to all the guys who contributed to it. I just
thought we might be able to exploit the richness and granularity of
MARC information a little further, and to ease the creation of new
MARC based site translators. Let me know about your views on the
subject. 

Thanks to Avram, Frank and Sylvain for their kind assistance.