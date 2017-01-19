# Echelle Archive

<b>allt20.dec.txt</b> (provided by D. Latham)<br>
The condordance table listing 33,909 unique targets.  I assigned unique target_id to each object in the list.

<br>
All the tables shown below can be joined by target_id.  However, we would need only df_simbad_selected.csv and df_prog_target.csv.

<b>df_basic_info.csv</b><br>
Basic information from the concordance table. These may not be that accurate.<br>
target_id, ra, pm_ra, dec, pm_dec, mag

<b>df_prog_target.csv</b><br>
Unique rows only, sorted by target_name and then prog_id.  This list shows, for a given target (i.e. target_id), what names were used in different programs<br>
prog_id, target_name, target_id

<b>df_simbad_selected.csv</b><br>
SIMBAD objects found and chosen to be used.<br>
target_id, rank, sep, simbad_identifier, ra, pm_ra, dec, pm_dec, ra_d, dec_d, plx, rv, z, magB, magV, sp_type
- sep: angular separation (in arcsed) between the concordance coordinates and the coordinates of matched SIMBAD objects.
- rank: 1 being smallest sep, 9 bieng greatest sep
- all other columns are taken from SIMBAD.

<b>df_simbad_unselected.csv</b><br>
SIMBAD objects found but not chosen to be used.<br>
target_id, rank, sep, simbad_identifier, ra, pm_ra, dec, pm_dec, ra_d, dec_d, plx, rv, z, magB, magV, sp_type

<br>
<b>Echelle_01.ipynb<br>
Just for fun.  Take a look at this if you want to know how I obtained the .csv files.
