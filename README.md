File-OSS-Scan version 0.01

DESCRIPTION
-----------
This module allows you to scan your project directory based on a set of pre-defined but also customizable rules, to detect all the used source files that originate from OSS ( or commercial software ). Unlike some of those commercial solutions for the OSS management, here we don't have to maintain a OSS code database, it means that we will not conduct code snippet match, and completely rely on the pattern match ( looking for a particular type of file, eg COPYING, LICENSE, or the existence of specific strings in file content, eg Copyright, LGPL License etc ).

SYNOPSIS
--------
    use File::OSS::Scan qw(:scan);

    scan_init( 'verbose' => 0, 'inflate' => 1 );

    scan_execute($proj_dir);
    my $ret = scan_result();

DEPENDENCIES
------------
This module requires Cache::FileCache for persistence of previous matching results.

INSTALLATION
------------
        perl Makefile.PL
        make
        make test
        make install

(I'd be lying if I said there was a real test suite at the moment...)
