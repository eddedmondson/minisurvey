# minisurvey
## Example code for making small astronomical surveys available with basic search capabilities on the web.

Like too much astronomy software, this'll need hacking for the individual case and isn't right now generally capable of doing everything in a nice way. Sorry! It's hopefully readable and simple enough to figure out though. It doesn't do anything fancy or clever. If you're trying to get a relatively small survey out on the web without going to SDSS-like lengths this should be pretty easy.

As to what constitutes 'small' - your survey catalogue should be small enough to exist as a flat file on your server and be reasonably downloadable in one go. This just gives a queryable interface.

It's a static db, there's no storage of user data or writing allowed (everything on the server should be read only).

Created for [xCOLD GASS](http://www.star.ucl.ac.uk/xCOLDGASS/).

Requires: 
* server end - php
* building - python modules astropy, sqlite3, pandas, numpy
* statically for your webpages - plotly and jquery

### To use:

create_sqlite.py ingests things like a catalogue FITS file (table extension) using astropy and ASCII tables using pandas  and outputs a SQLite database.

Code in example/ is php code that can query the resulting .db file.
