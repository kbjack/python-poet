README
======

About
------
  This is a poetry generator written in Python. It is for the OSU Valley
Library's Crafternoon events to show people the connection between technology
and creativity. This code is meant to be customized, from the words in the
word-type files to the sentence structures.

Word-Type Files
---------------
  The files named for word-types (i.e. Nouns, Verbs) contain lists of words of
that word type. They are meant to be added to in order to give the generator a
larger vocabulary. Some of these files contain two lists of words, one for
singular and one for plural. The two lists don't have to contain the same words
or the same number of words as they are both pulled from individually, but in
order for the sentences to sound correct, only the plural form of words should
be put in the plural list, and only the singular form of words should be put in
the singular list. New word types should be given their own file, included in
poetry.py following the structure of the other word-types, and added as inputs
to all sentence structures and stanza.

Sentence File
-------------
  The sentence file contains all the available sentence structures. When a new
sentence structure is added, the function name must be added to the options hash
in poetry.py. If it is not, the sentence structure will never be chosen. New
sentence structures must accept all word-types, as well as self.
  The sentence structure chosen is randomized in stanzas.py.
  The Sentences file also contains the randomization of the selection of words
for the sentence structure. The selection is pseudo-random and could be improved
on. As well as single word randomization to be called by sentence structures,
sentences also contains the structure for similes. This is extracted from the
sentence structure because it could be reused in a variety of sentence
structures.

Poetry File
-----------
  The Poetry file imports all word types, sentences, and stanzas. It then
initializes all the aforementioned classes. It contains all of the options for
sentences to be chosen. New sentence structures added need to be added to the
options hash. Finally, the Poetry file contains the print poem function. This
function prints the number of stanzas containing the number of lines desired.

Running the Poetry Generator
----------------------------
  To run the Poetry Generator, download all of the files. Then, in the directory
containing the files, run `python poetry.py`
  To change the length of the poem or the stanza, run `python poetry.py
[numStanzas] [numLines]`
  To save the poem to a file, run `python poetry.py > file_name` or `python
poetry.py [numStanzas] [numLines]`
  Note: running the above more than once with the same filename will overwrite
the original run.

Contributing
-------------
  Please contribute!
  Feel free to fork, or to branch and create pull requests!
