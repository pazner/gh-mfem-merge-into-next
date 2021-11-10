Install by running
```
gh extension install pazner/gh-mfem-merge-into-next
```

(You can also install by closing the repository and running `gh extension install .` from within the repository directory.)

Run with
```
gh mfem-merge-into-next <pr-number>
```
from a (clean) copy of the MFEM repository.

This will:

* Make sure the repository state is clean
* Check out `next` and pull the latest changes
* Check out the given PR into a temporary branch
* Run the `branch-history` check
* Merge the PR into next with an informative message
* Delete the temporary branch

After this process completes successfully, run `git push` to push changes.
