# Changelog

## Unreleased

### Changed

- changed the function sanitize_column_names() to sanitize() which now takes just a array of strings and 'sanitizes' them; Introduced Breaking Changes
- rewrote tests in a cleaner way
- renamed the function suggest_col_drop() to spot_irrelevant_columns()

### Fixed

- bug fixed in the change_dtypes() function; bug fixes in the suggest_col_drop() function => identifying the 'id' columns like customer id, id, ... but NOT columns like rfid

## 0.2.1

### Fixed

- fixed multiple underscore issue and add support for
  mulitple consecutive capital letters (DNSServer -> dns_server) in CamelCase to snake_case conversion

## 0.2.0

### Added

- add default parameters to preprocess function
- add parameter 'label_col' in preprocess() to remove
  rows where the label_col is null
- add parameter 'label_col' in remove_outliers() so that
  the label col will not be considered as a column to remove outliers from
- add suggest_col_drop() to suggest which columns to drop (irrelevant columns) based on the column name; like ID, first_name, surname, ...

### Changed

- sanitize_column_names() now converts CamelCase to snake_case
- suggest_conversion_dict() now suggests 'category' dtype to numeric columns that are actually categorical; like 'has_credit_card' that has 1 or 0 as values

## 0.1.1

### Changed

- sanitize_column_names now keeps any already present underscores

## 0.1.0

### Added

- add MIT license badge in readme
- add function to suggest conversion dict

## 0.0.1

- work in progress