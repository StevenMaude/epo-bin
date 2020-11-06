# epo-bin

A daily collection of Garmin's `EPO.BIN` GPS data used for faster GPS
locking on Garmin watches.

It uses
[`armstrong`](https://github.com/StevenMaude/armstrong) and runs via
GitHub Actions.

Output is stored in the
[`epo-bin`](https://github.com/StevenMaude/epo-bin/tree/epo-bin) branch.
This branch is force pushed after a successful collection of the
`EPO.BIN` file.

## Download `EPO.BIN`

Download the latest
[EPO.BIN](https://github.com/StevenMaude/epo-bin/raw/epo-bin/EPO.BIN).

## (Why force push to a branch?)

I had considered either storing in the `main` branch and amending the
commit that adds `EPO.BIN`, or using GitHub releases to store `EPO.BIN`.

Force pushing to a dedicated branch simplfies this:

* It is simpler than managing GitHub releases, which are tied to tags,
  and old releases should be deleted since the latest `EPO.BIN`
  supplants older versions.
* It avoids inflating the repository by committing binary files
  repeatedly; we only keep the latest.
* The `main` branch can be developed without being force pushed.
