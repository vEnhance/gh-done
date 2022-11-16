# gh-done

Trivial wrapper which closes an issue and adds a comment "Finished in `...`.".

## Usage

- `gh done 42` will close issue #42 and add a comment "Finished in [insert SHA
  of current HEAD]"

- `gh done 42 HEAD~5` will close issue #42 and add a comment "Finished in [insert SHA
  of HEAD~5]"

In general, the arguments after the first can be any arguments (even more than one)
accepted by `git rev-parse`.

By default, the script will show the issue and the commit before sending the
bits off into the internets. Pass `--quiet` before any other argument to stop
this behavior (or pipe `yes`).
