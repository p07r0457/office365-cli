# aad o365group report activitydetail

Get details about Office 365 Groups activity by group.

## Usage

```sh
aad o365group report activitydetail [options]
```

## Options

Option|Description
------|-----------
`--help`|output usage information
`-p, --period [period]`|The length of time over which the report is aggregated. Supported values `D7|D30|D90|D180`. Specify the `period` or `date`, but not both.
`-d, --date [date]`|The date for which you would like to view the users who performed any activity. Supported date format is `YYYY-MM-DD`. Specify the `date` or `period`, but not both.
`-f, --outputFile [outputFile]`|Path to the file where the Office 365 Groups activity by group report should be stored in
`-o, --output [output]`|Output type. `text|json`. Default `text`
`--verbose`|Runs command with verbose logging
`--debug`|Runs command with debug logging

## Examples

Get details about Office 365 Groups activity by group for the last week

```sh
aad o365group report activitydetail --period D7
```

Get details about Office 365 Groups activity by group for September 09, 2019

```sh
aad o365group report activitydetail --date 2019-09-28
```

Get details about Office 365 Groups activity by group for the last week and exports the report data in the specified path in text format

```sh
aad o365group report activitydetail --period D7 --output text --outputFile './o365groupactivitydetail.txt'
```

Get details about Office 365 Groups activity by group for the last week and exports the report data in the specified path in json format

```sh
aad o365group report activitydetail --period D7 --output json --outputFile './o365groupactivitydetail.json'
```
