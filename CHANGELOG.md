# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Most recent change on the bottom.

## [Unreleased]
- examples of `end_of_epoch_callbacks` are listed in nequip.train.callbacks

## [0.3.1]
### Fixed
- `iepoch` is no longer off-by-one when restarting a training run that hit `max_epochs`
- Builders, and not just sub-builders, use the class name as a default prefix
### Added
- `early_stopping_xxx` arguments added to enable early stop for platued values or values that out of lower/upper bounds.

## [0.3.0] - 2021-05-07
### Added
- Sub-builders can be skipped in `instantiate` by setting them to `None`
- More flexible model initialization
- Add MD w/ Nequip-ASE-calculator + run-MD script w/ custom Nose-Hoover

### Changed
- PBC must be explicit if a cell is provided
- Training now uses atomic file writes to avoid corruption if interupted
- `feature_embedding` renamed to `chemical_embedding` in default models

### Fixed
- `BesselBasis` now works on GPU when `trainable=False`
- Dataset `extra_fixed_fields` are now added even if `get_data()` returns `AtomicData` objects

## [0.2.1] - 2021-05-03
### Fixed
- `load_deployed_model` now correctly loads all metadata

## [0.2.0] - 2021-04-30