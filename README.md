## Where do the changes during merge conflicts go and how can I isolate them?

Feature branch change a Ham Sandwish to PBJ, but during merge resolution, it's
decided to settle for BLT to suit all requirements. (This is intended to
mimic resolving a merge where we have to materially change how both merging 
codebases operate wrt their original feature branch implementations in order
to get a to correct overall operation with both features.)

Take a look at the difference between `git log --stat` and `git show HEAD
6650e9a`.  The former doesn't really call out the fact that `sandwich` was
extensively edited beyond the changes from the two merge parents, yet the
latter clearly has the changeset. 
