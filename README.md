# Perstem:  Persian stemmer, morphological analyzer, transliterator


Persian (Farsi) stemmer, morphological analyzer, transliterator, and partial
part-of-speech tagger.  Input may be encoded as Perso-Arabic script UTF-8,
ISIRI 3342, Windows-1256, SGML/HTML/XML-style numeric character references (ncr),
or dehdari-transliterated latin-script text.  Use the -i flag to specify input
encoding.  Output is handled similarly.


## Usage
      perl perstem.pl [options] < input > output

## Options
     -f, --form <x>         Output forms as one of the following:
                              dict: as they appear in a dictionary (default)
                              linked: show all morphemes, linked together
                              unlinked: show all morphemes as separate tokens
                              untouched: don't stem/analyze; mostly for char-set conversion
         --flush            Autoflush buffer output after every line
     -h, --help             Print this usage
     -i, --input <type>     Input character encoding type {cp1256,isiri3342,ncr,
                            translit,utf8} (default: utf8)
         --irreg-stem {0|1} Resolve irregular present-tense verb stems to their
                            past-tense stems (eg. kon -> kar).  (default: 1 == true)
     -n, --noroman          Delete all non-Arabic script characters (eg. HTML tags)
     -o, --output <type>    Output character encoding type {arabtex,cp1256,
                            isiri3342,ncr,translit,utf8} (default: utf8)
     -p, --pos              Tag inflected words for parts of speech
         --pos-sep <char>   Separate words from their parts of speech by <char>
                            (default: "/" )
     -r, --recall           Increase recall by parsing ambiguous affixes; may lower
                            precision
         --skip-comments    Skip commented-out lines, without printing them
     -s, --stem             Return only word stems
     -t, --tokenize {0|1}   Tokenize punctuation (default: 1 == true)
     -u, --unvowel          Remove short vowels
     -v, --version          Print version
     -z, --zwnj {0|1}       Insert Zero Width Non-Joiners where they should be (default: 1 == true)



## Acknowledgements
Thanks to Jace Livingston, David Zajic, and Corey Miller for their comprehensive error
analysis and other suggestions.  Thanks to Jay Ritch and Artyom Lukanin for spotting bugs.


## Citation
If you use this software please cite the following

Dehdari, Jon, and Deryle Lonsdale. 2008. A link grammar parser for Persian. In Karimi, S., Samiian, V., and Stilo, D., editors, *Aspects of Iranian Linguistics*, volume 1. Cambridge Scholars Press. ISBN: 978-18-471-8639-3 ([BibTeX](http://jon.dehdari.org/pubs/bib/dehdarilonsdale2005.bib.txt))

Jadidinejad, Amir Hossein, Fariborz Mahmoudi, and Jon Dehdari. 2010. Evaluation of Perstem: A Simple and Efficient Stemming Algorithm for Persian. In Peters, C., Nunzio, G. D., Kurimo, M., Mandl, T., Mostefa, D., Peñas, A., and Roda, G., editors, *Multilingual Information Access Evaluation I. Text Retrieval Experiments*, volume 6241 of Lecture Notes in Computer Science, pages 98–101. Springer, Heidelberg. ([BibTeX](http://jon.dehdari.org/pubs/bib/jadidi-etal2010.bib.txt))
