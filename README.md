# NAME

Plack::Debugger::Panel::DBIProfile

# VERSION

version 0.01

# SYNOPSIS

    my $debugger = Plack::Debugger->new(
        panels => [
            Plack::Debugger::Panel::DBIProfile->new(),
            ... etc.
        ],

# DESCRIPTION

This piece of blatant thievery is a port of [Plack::Middleware::Debug::DBIProfile](https://metacpan.org/pod/Plack::Middleware::Debug::DBIProfile)
to [Plack::Debugger](https://metacpan.org/pod/Plack::Debugger).

## `new`

Accepts two optional parameters in addition to those documented in [Plack::Debugger](https://metacpan.org/pod/Plack::Debugger).

- `dbi_profile`

    Default: 6

    See [https://metacpan.org/pod/DBI::Profile#ENABLING-A-PROFILE](https://metacpan.org/pod/DBI::Profile#ENABLING-A-PROFILE).

- `dbi_profile_format`

    Default: `%1$s XXX %11$fs / %10$d = %2$fs avg (first %12$fs, min %13$fs, max %14$fs`

    See [https://metacpan.org/pod/DBI::Profile#as\_text](https://metacpan.org/pod/DBI::Profile#as_text), but note that the format must
    include 'XXX'. We split on the XXX and place the pair in succeeding rows of the
    debugger panel.

# AUTHOR

Dave Baird &lt;dave@zerofive.co.uk>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2016 by David R. Baird.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
