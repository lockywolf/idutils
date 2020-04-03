2020-04-03, lockywolf
I managed to build it by endlessly mindlessly repeating 
gnulib/autoconf commands.

So far things should work with just:
1. ./configure
2. make
3. use your package manager to pack it

Below is obsolete. I keep it here, because it will be very likely
that similar magic will have to be done again. Cargo cult programming,
you know.
So far the most successful route has been like this:

1. git checkout gnulib (from whereever GNU people keep it)
2. git checkout idutils
3. cd idutils
4. ./configure
5. make
4. ../gnulib/gnulib-tool --add-index
5. make 
