# fetchdoi

`fetchdoi` is a small python script that takes a DOI and appends the bibtex entry for it to a provided file. If no file is provided it will append to `./library.bib`.

## Usage

In mac or linux, the file `fetchdoi.py` can be added to `/home/<username>/bin/` and then from the terminal:

```
fetchdoi.py 10.21105/joss.01880  ./mylibrary.bib
```

will add the bibtex entry for the journal article for my (shameless plug) `R` package [rnassqs]() to the file `mylibrary.bib`.

I also add an alias in my `.bashrc` file:

```
# .bashrc
alias doi=~/bin/fetchdoi.py
```

so that in termanals I can fetch a bibtex entry with `doi <DOI>`.

By default the script uses the bibtex key `<Lastname1><Lastname2><Year>`. If there are more than two authors it uses `<Lastname1>ETAL<Year>`.


