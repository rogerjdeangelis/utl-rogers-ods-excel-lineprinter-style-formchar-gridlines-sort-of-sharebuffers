# utl-rogers-ods-excel-lineprinter-style-formchar-gridlines-sort-of-sharebuffers
Rogers ods lineprinter style like formchar gridlines sort of sharebuffers
    %let pgm=utl-rogers-ods-excel-lineprinter-style-formchar-gridlines-sort-of-sharebuffers;

    Rogers ods lineprinter style like formchar gridlines sort of sharebuffers;

    github
    https://tinyurl.com/bdezedzb
    https://github.com/rogerjdeangelis/utl-rogers-ods-excel-lineprinter-style-formchar-gridlines-sort-of-sharebuffers

    Kind of hokey but I need this for documentation purposes.

    You do need to do some manual editing to cut and  add variable names.
    Much easier than edition the ods slick output.

    related
    github
    https://tinyurl.com/yark4rdu
    https://github.com/rogerjdeangelis/utl_editing_a_sas_transport_file_in_place_sharebuffers


    /*               _     _
     _ __  _ __ ___ | |__ | | ___ _ __ ___
    | `_ \| `__/ _ \| `_ \| |/ _ \ `_ ` _ \
    | |_) | | | (_) | |_) | |  __/ | | | | |
    | .__/|_|  \___/|_.__/|_|\___|_| |_| |_|
    |_|
    */

    /**************************************************************************************************************************/
    /*                                         |                                                                              */
    /*            INPUT                        |                        OUTPUT                                                */
    /*            ====                         |                        ======                                                */
    /*                                         |                                                                              */
    /*   SASHELP.CLASS                         |                                                                              */
    /*                                         |                                                                              */
    /*   NAME     SEX AGE  HEIGHT WEIGHT       |     -----------------------+                                                 */
    /*                                         |     | A1  | fx    | NAME   |                                                 */
    /*   Alfred    M   14   69.0   112.5       |     -------------------------------------------------------                  */
    /*   Alice     F   13   56.5    84.0       |     [_]|    A     |    B    |    C    |    E    |    F    |                  */
    /*   Barbara   F   13   65.3    98.0       |     -------------------------------------------------------                  */
    /*   Carol     F   14   62.8   102.5       |      1 | NAME     |   AGE   |   SEX   |  HEIGHT |  WEIGHT |                  */
    /*   Henry     M   14   63.5   102.5       |     -- |----------+---------+---------+---------+---------+                  */
    /*   James     M   12   57.3    83.0       |      2 | Alfred   |M        |14       |69       |112.5    |                  */
    /*                                         |     -- |----------+---------+---------+---------+---------+                  */
    /*                                         |      3 | Alice    |F        |13       |56.5     |84       |                  */
    /*                                         |     -- |----------+---------+---------+---------+---------+                  */
    /*                                         |      4 | Barbara  |F        |13       |65.3     |98       |                  */
    /*                                         |     -- |----------+---------+---------+---------+---------+                  */
    /*                                         |      5 | Carol    |F        |14       |62.8     |102.5    |                  */
    /*                                         |     -- |----------+---------+---------+---------+---------+                  */
    /*                                         |      6 | Henry    |M        |14       |63.5     |102.5    |                  */
    /*                                         |     -- |----------+---------+---------+---------+---------+                  */
    /*                                         |      7 | James    |M        |12       |57.3     |83       |                  */
    /*                                         |     -- |----------+---------+---------+---------+---------+                  */
    /*                                         |     [CLASS]                                                                  */
    /*                                         |                                                                              */
    /*                                         |                                                                              */
    /**************************************************************************************************************************/

    /*                   _
    (_)_ __  _ __  _   _| |_
    | | `_ \| `_ \| | | | __|
    | | | | | |_) | |_| | |_
    |_|_| |_| .__/ \__,_|\__|
            |_|
    */

     SASHELP.CLASS

    /*
     _ __  _ __ ___   ___ ___  ___ ___
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|
    | |_) | | | (_) | (_|  __/\__ \__ \
    | .__/|_|  \___/ \___\___||___/___/
    |_|
    */

    NOTE: Because of sharebuffers you have to recreate
          the temp file each time you run.
          The code updates the input.

    /*                       _       _
    | |_ ___ _ __ ___  _ __ | | __ _| |_ ___
    | __/ _ \ `_ ` _ \| `_ \| |/ _` | __/ _ \
    | ||  __/ | | | | | |_) | | (_| | ||  __/
     \__\___|_| |_| |_| .__/|_|\__,_|\__\___|
                      |_|
    */

    filename tmp temp;
    data _mull_;
      file tmp;
      input;
      put _infile_;
      putlog _infile_;
    cards4;
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
     2 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
     3 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
     4 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
     5 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
     6 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
     7 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
     8 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
     9 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
    10 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
    11 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
    12 |          |                   |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
    13 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
    14 |          |         |         |         |         |         |         |         |         |         |
    -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|
    15 |          |         |         |         |         |         |         |         |         |         |
    --------------------------------------------------------------------------------------------------------+
    ;;;;
    run;quit;

    /*__ _ _ _            _ _
     / _(_) | |   ___ ___| | |___
    | |_| | | |  / __/ _ \ | / __|
    |  _| | | | | (_|  __/ | \__ \
    |_| |_|_|_|  \___\___|_|_|___/

    */

    data _null_;
      set sd1.have;
      infile tmp sharebuffers;
      file tmp;
      input;
      put _infile_;
      input;
      set sashelp.class (Obs=6) point=_n_ nobs=numobs;
      put @6 name @16 sex @26 age @36 height @46 weight;
      call symput('lines',2*_n_+1);
    run;quit;

    data _null_;
      infile tmp;
      input;
      if _n_=1 then do;
         put "-----------------------+";
         put "| A1  | fx    | NAME   |";
         put "--------------------------------------------------------------------------------------------------------+";
         put "[_]|    A     |    B    |    C    |    E    |    F    |    G    |    H    |    I    |    J    |    K    |";
         put "--------------------------------------------------------------------------------------------------------|"
         PUT " 1 | NAME     |   AGE   |   SEX   |  HEIGHT |  WEIGHT |         |         |         |         |         |";
      end;
      put _infile_;
      if _n_=&lines then do;
         put '[CLASS}';
         stop;
      end;
    run;quit;

    /*           _               _
      ___  _   _| |_ _ __  _   _| |_
     / _ \| | | | __| `_ \| | | | __|
    | (_) | |_| | |_| |_) | |_| | |_
     \___/ \__,_|\__| .__/ \__,_|\__|
                    |_|
    */

    /**************************************************************************************************************************/
    /*                                                                                                                        */
    /* -----------------------+                                                                                               */
    /* | A1  | fx    | NAME   |                                                                                               */
    /* --------------------------------------------------------------------------------------------------------+              */
    /* [_]|    A     |    B    |    C    |    E    |    F    |    G    |    H    |    I    |    J    |    K    |              */
    /* --------------------------------------------------------------------------------------------------------|.             */
    /*  1 | NAME     |   AGE   |   SEX   |  HEIGHT |  WEIGHT |         |         |         |         |         |              */
    /* -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|              */
    /*  2 | Alfred   |M        |14       |69       |112.5    |         |         |         |         |         |              */
    /* -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|              */
    /*  3 | Alice    |F        |13       |56.5     |84       |         |         |         |         |         |              */
    /* -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|              */
    /*  4 | Barbara  |F        |13       |65.3     |98       |         |         |         |         |         |              */
    /* -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|              */
    /*  5 | Carol    |F        |14       |62.8     |102.5    |         |         |         |         |         |              */
    /* -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|              */
    /*  6 | Henry    |M        |14       |63.5     |102.5    |         |         |         |         |         |              */
    /* -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|              */
    /*  7 | James    |M        |12       |57.3     |83       |         |         |         |         |         |              */
    /* -- |----------+---------+---------+---------+---------+---------+---------+---------+---------+---------|              */
    /* [CLASS}                                                                                                                */
    /*                                                                                                                        */
    /*                                                                                                                        */
    /**************************************************************************************************************************/

    /*              _
      ___ _ __   __| |
     / _ \ `_ \ / _` |
    |  __/ | | | (_| |
     \___|_| |_|\__,_|

    */
