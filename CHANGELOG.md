## CHANGELOG

#### 0.5.14

* Fixed detections and handling of files with upper or mixed case extensions.

#### 0.5.13

* Fixed a bug where millstone would hang if an absolute path to a shapefile was used and that
  shapefile did not exist at that path.

#### 0.5.12

* Added command line millstone tool
* Added support for reading any supported file in .zip archives
* Better error messages if broken symlinks are encountered
* Support added for downloading images at urls without clear image file extensions
* Fixed handling of hidden files in zip archives
* Switched to using console.error for log output

#### 0.5.11

* Will now throw if files do not exist (instead of throwing on missing/unknown srs)

* Fixed support for loading layer datasource files from alternative windows drives

* Moved to no-symlink/no-copy behavior on all windows versions

* Updated node-srs version

* Improved handling of known file extensions to better support guessing extensions via headers

* Fixed handling of sqlite attach with absolute paths

#### 0.5.10

* Fixed missing error handling when localizing Carto URIs

#### 0.5.9

* Improved uri regex methods for carto urls - #68, #69, #70, #72, and #73

* Use copy fallback on Windows platforms supporting symlinks but where the user does not have the symlink 'right' (#71)

* Restored Node v0.4.x support

#### 0.5.8

* Improved uri regex methods for carto urls - amends #63

#### 0.5.7

* Fixed handling of multiple non-unique carto urls in the same stylesheet (#63)

#### 0.5.6

* Fixed extension handling for urls without an extension

* Moved to streaming copy of data when in copy mode to avoid too much memory usage

* Fixed race condition when localizing imag/svg icons in styles like point-file and marker-file.

* Exposed the global downloads object so calling applications can see how many downloads millstone is currently handling

* Removed node v0.8.x deprecation warnings

* Added more agressive re-copying of data when it is out of date and millstone is in copy mode (win XP)

* Moved to processing shapefile parts instead of the directory

#### 0.5.5

* Added a verbose mode that can be trigged by setting NODE_ENV = 'development'

* Switched to request (dropped node-get) for better proxy support

* Support for making relative the paths stored to the download cache

* Support for zipfiles with no extension

* Advertise node v8 support

#### 0.5.4

* Fixes to better support localization of carto resources

#### 0.5.3

* Updated node-get min version in order to fully support proxy auth
* Improved cross-platform relative path detection

#### 0.5.2

* Improved regex used to detect content-disposition

* Support for localizing uri's in stylesheet

#### 0.5.1

* Moved to mocha for tests

* Made `nosymlink` option optional

#### 0.5.0

* Add `nosymlink` option for not downloading files