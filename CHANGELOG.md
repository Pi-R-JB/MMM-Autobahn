# Changelog

All notable changes to this maintained fork of MMM-Autobahn are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project follows Semantic Versioning.

## [1.1.0] - 2026-09-01

### Added

- Route-based traffic filtering using configurable latitude/longitude route points.
- Configurable route corridor width via `corridorKm`.
- Support for Autobahn API `LineString` geometry with fallback to a warning's single coordinate.
- Time-based reload schedules via `reloadSchedule`.
- Schedule handling for time windows that cross midnight.
- Compact warning display with configurable `maxDescriptionLines`.
- Distinct UI states for loading, successful empty results, and API request failures.
- `.gitignore` for common local files.

### Changed

- API requests now use native `fetch()` with a 60-second timeout.
- Warning filtering now prefers geometry-based route matching when a route is configured.
- Long warning descriptions are rendered more compactly to reduce overlap with neighbouring MagicMirror modules.
- Documentation was restructured and updated for the current Autobahn API.

### Fixed

- Prevented crashes when warning titles do not contain junction numbers.
- Improved compatibility with current Autobahn API responses where junction numbers are no longer reliably included in warning titles.
- Legacy `from` / `to` filtering remains available for backwards compatibility.

## [1.0.0]

Original release by [JockeyDoe](https://github.com/JockeyDoe/MMM-Autobahn).
