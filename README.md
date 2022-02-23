# Overview

This repository contains some tools to create the control tables required
for running INDIs and their associated SQL scripts directly from command line.

The sources are stored in AWS along with the test environment in
s3://nameservice/releases/dbdir-tools/

# Features

* Wide spreadsheet support

All different kind of spreadsheet formats supported. All kinds of spreadsheets
which can be handled by Spreadsheet::Read can be read.

* Two step approach for DBDIR spreadsheet handling

First step converts XLS into dbdir.tab, tables.tab, units.tab.
Second step creates SQL command files from the 3 tab files.

* Perl based

Perl based and therefore portable.

* No static template files required

* No hard coded stuff

Exception: The spreadsheet is parsed positional.

* Removal of LONG

Replaced by CLOB/TEXT

* Postgres support

* Consistency check

Spreadsheet is checked for consistency

* CI/CD support

Can be used by Jenkins

* Documentation included

The documentation of the programs is included and can be reached either 
via `perldoc <program>` or `<program> -m`

* Meaningful error messages

# Removed features

* NST creation

The NST creation is only done for the required "ERSTEINTRAG" fields. All other
fields are ignored and won't be injected.

# Todo

* Log4Perl Support

log4perl should be supported.

* Tablespace Support

Tablespace names can be defined in Spreadsheet

* Additional indexes
  * Unique Indexes
  * Composite Indexes
  * Unique Composite Indices


