# fetch-elmer-keys
Fetch keywords from Elmerfem sif files and output them in SOLVER.KEYWORDS format

For example finding keywords that are in the sif files (located in the subdirectories of the current directory) but not in the SOLVER.KEYWORDS file:

    $ find -name "*.sif" | fetch-elmer-keys -o keysout.txt
    $ fldiffs -f keysout.txt $ELMER_HOME/share/elmersolver/lib/SOLVER.KEYWORDS
