# condastats-data

Mirrored [Anaconda public package download data](https://github.com/ContinuumIO/anaconda-package-data)
(monthly Parquet files) served via GitHub Pages for the
[condastats](https://github.com/conda-incubator/condastats) browser demo.

## How it works

A [scheduled GitHub Action](.github/workflows/sync.yml) runs monthly to sync
Parquet files from `s3://anaconda-package-data/conda/monthly/` and publishes
them to the `gh-pages` branch using an orphan commit (no history accumulation).

The files are then available at:

```
https://conda-incubator.github.io/condastats-data/{year}/{year}-{month}.parquet
```

For example:

```
https://conda-incubator.github.io/condastats-data/2025/2025-01.parquet
```

## Data license

The Anaconda package download data is licensed under
[CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) by Anaconda, Inc.
