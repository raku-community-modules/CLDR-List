[![Actions Status](https://github.com/raku-community-modules/CLDR-List/actions/workflows/linux.yml/badge.svg)](https://github.com/raku-community-modules/CLDR-List/actions) [![Actions Status](https://github.com/raku-community-modules/CLDR-List/actions/workflows/macos.yml/badge.svg)](https://github.com/raku-community-modules/CLDR-List/actions) [![Actions Status](https://github.com/raku-community-modules/CLDR-List/actions/workflows/windows.yml/badge.svg)](https://github.com/raku-community-modules/CLDR-List/actions)

NAME
====

CLDR::List - Localized list formatters using the Unicode CLDR

SYNOPSIS
========

```raku
use CLDR::List;

my $list  = CLDR::List.new(locale => 'en');
my @fruit = <apples oranges bananas>;

say $list.format(@fruit);      # apples, oranges, and bananas

$list.locale = 'en-GB';        # British English
say $list.format(@fruit);      # apples, oranges and bananas

$list.locale = 'zh-Hant';      # Traditional Chinese
say $list.format('１'..'４');  # １、２、３和４
```

DESCRIPTION
===========

Localized list formatters using the Unicode CLDR.

Attributes
----------

  * locale

Methods
-------

  * format

SEE ALSO
========

  * * [List Patterns in UTS #35: Unicode LDML](http://www.unicode.org/reports/tr35/tr35-general.html#ListPatterns)

  * * [Perl Advent Calendar: CLDR TL;DR](http://perladvent.org/2014/2014-12-23.html)

  * * [Unicode beyond just characters: Localization with the CLDR](http://patch.codes/talks/localization-with-the-unicode-cldr/) (video and slides)

AUTHOR
======

Nova Patch

COPYRIGHT AND LICENSE
=====================

Copyright 2013 – 2017 Nova Patch

Copyright 2024 Raku Community

This library is free software; you can redistribute it and/or modify it under the same terms as Perl itself.

