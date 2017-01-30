Mail Management Tools
=====================

This repository has some scripts to manage MTAs queue or so on.

- `qq-manage`: qmail queue management script written in Perl.
- `pq-manage`: Postfix queue management script written in Perl.

## Installation
Just copy a script into anywhere in a server. These scripts should work with Perl 5.8 or newer.

## Example

This example is `qq-manage` one but almost same in `pq-manage`.

```shellsession
$ # check queue statistics
$ qq-manage -s
$ # list "remote" mail queue messages
$ qq-manage -l -R
$ # list "remote" mail queue messages which have 'From: spam@example.com' header
$ qq-manage -t -R header 'From: spam\@example\.com'
$ # delete "remote" mail queue messages which have 'From: spam@example.com' header
$ qq-manage -d -R header 'From: spam\@example\.com'
```

Please see each scripts' help for more details

## License
These scripts are licensed under MIT. See the [LICENSE][license] file for details.

[license]: https://github.com/tsukaeru/mail-management-scripts/blob/master/LICENSE
