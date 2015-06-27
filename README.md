GPG Find Passphrase
===================

Finds the valid GPG passphrase from lines of passphrase guesses.


Usage
-----

Given a GPG user "John Smith" with private key passphrase of "Pa55word" and the
following passphrase guesses file:

    $ echo "password
      Password
      Pa55word
      Passw0rd" > guesses

Then the following command will find the passphase which is valid:

    $ cat guesses | gpg-find-passphrase 'John Smith'

The output of gpg-find-passphrase is the input line which is a valid passphrase
(in the above example it would be "Pa55word"). If no passphrase is valid then
there is no output.


License
-------

Copyright 2015 Nathan Jones

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.
