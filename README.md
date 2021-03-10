# Project 2

Apply cryptographic primitives to design and implement a client application for a secure file sharing system.  (Drive with files secured so server cannot view or tamper with data.)

Written in Golang

Requirements:

    1. Authenticates with username and password
    2. Save files to server
    3. Load saved files from server
    4. Overwrite saved files on the server
    5. Append to saved files on server
    6. Share saved files with other users
    7. Revoke access to previously shared files

Two servers provided, Keystore and Datastore

    Keystore - trusted server where users publish their public keys.
    Attackers cannot overwrite any entry in Keystore.

    Key-value store: key is unique id used to index the value in database, not crypto key.

    Datastore - untrusted server that provides persistent storage
    Not safe, data stored must have confidentiality and integrity stored for anything sensitive.

    Key-value access same as above.
    Whatever you store here, needs to be well protected.  Maybe a user fetches an item from a datastore, finds the appropriate keystore, then verifies authenticity.  If authentic, then the datastore should be int and conf, so safe to open.
	
Some cryptographic algorithms already implemented in userlib.

Starter code contains 8 functions in proj2.go that must be implemented.  Read pg0 for details.


