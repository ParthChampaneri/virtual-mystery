# Mystery Framework

## Usage

NOTE: All of these requests require an authentication token in the header.

** Definition **

Get a list of release data ordered by release number upto and including the current release.

** Request **

`GET /mystery/release/list>`

** Response **

 - 200 OK on Success
 - 400 BAD REQUEST on Failure

JSON:

 [
     {
        "commented": boolean,
        "number": releasenumber
     }
 ]

** Definition **

Get information on the artifact for the requested release. 

** Request **

`GET /mystery/release/<release#>`

** Response **

 - 200 OK on Success
 - 400 BAD REQUEST on Failure

JSON:

 [
     {
        "clue": cluetext,
        "hash": releasehash,
	"mystery_hash": mysteryhash
     }
 ]