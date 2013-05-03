Introduction
============




ooc code is compiled to C using [https://github.com/nddrylliog/rock rock]

The rock [https://github.com/nddrylliog/rock github page] contains a list of high-level dependencies and more detail for [https://github.com/nddrylliog/rock/blob/master/INSTALL UNIX] and [https://github.com/nddrylliog/rock/blob/master/INSTALL.win32 Windows].

== Installing in Ubuntu Linux ==

==== Boehm GC (optional) ==== 
1. Download the [http://www.hpl.hp.com/personal/Hans_Boehm/gc/ Boehm GC] from [http://www.hpl.hp.com/personal/Hans_Boehm/gc/gc_source/gc.tar.gz here].

2. Configure, compile and install
  ./configure [--prefix=/<alternate path>]
  make
  make install

==== rock ====
3. Download and compile rock
  git clone https://github.com/nddrylliog/rock.git rock
  cd rock
  make rescue


The first time you compile ooc source with rock will take a little longer than subsequent builds because of the nature of the compilation to C99 followed by compilation of C process. In the .libs directory - that is created wherever you call rock - the compiler will produce not only C code for your ooc but also produce the C code for the language constructs used by your code under .libs/ooc/sdk. Future compiles (especially those that do not use additional language features or parts of the sdk) will be significantly more spritely. Enjoy!
