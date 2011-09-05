# Test Driven Enlightenment

# Intended Audience

Anybody who wants to learn more about testing software to improve its awesomeness.

# Reviewer Guidelines

I appreciate all suggestions and critiques, especially:

 * Is the work accurate?
 * Is the work complete?
 * Is the work coherent?
 * Are there missing sections and subjects?
 * Are the examples effective?
 * Is the flow of information appropriate?

# Building this Book

You need a modern version of Perl installed.  I recommend Perl 5.10.1, but
anything newer than 5.8.6 should work.

You should also have Pod::PseudoPod 0.16 or newer installed with its
dependencies.

From the top level directory of a checkout, build the individual chapters with:

    $ perl build/tools/build_chapters.pl

The chapter sources are in the sections/ directory.  Each chapter has a
corresponding chapter_nn.pod file.  Each file contains multiple POD links which
refer to other files in the sections/ directory.  Each of those files contains
a PseudoPOD Z<> anchor.

The build_chapters.pl program weaves these sections into chapters and writes
them to POD files in build/chapters.

(This process makes it easy to rearrange sections within and between chapters
without generating huge diffs.)

To build HTML from these woven chapters:

    $ perl build/tools/build_html.pl

This will produce nicely-formatted HTML in the build/html/ directory.  If
anything looks wrong, it's a mistake on my part (or a CSS problem) and patches
are very welcome.

To build an ePub eBook from the woven chapters:

    $ perl build/tools/build_epub.pl

This will produce an ePub eBook in the build/epub/ directory.

To build PDFs from the chapters:

    $ perl build/tools/build_pdf.pl

This will build PDFs in the build/pdf directory.  You must have App::pod2pdf
installed from the CPAN.


# Contributing to Test Drive Enlightenment

This work is licensed under a Creative Commons Attribution-Noncommercial-Share
Alike 3.0 United States License.  For more details, see:

    http://creativecommons.org/licenses/by-nc-sa/3.0/us/

Please feel free to point people to this repository. Suggestions and
contributions are welcome. You have the right to redistribute modified
versions, but I ask (though do not require) you to file bugs or submit pull
requests against this repository.

This book is available in print and in formatted electronic formats
from Onyx Neon Press:

    http://www.onyxneon.com/books/REAL_SOON_NOW

The electronic versions are available for free, with no restrictions on free
redistribution.
