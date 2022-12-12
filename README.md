## IPFS Upload - CLI tool intended for web3.storage

The rationale for this project is the fact that https://web3.storage seems to be bottle-necked when trying to handle user uploads through the UI that are moderately large and fails outright or uploads incomplete files. This script is intended to give more visibility and control over file uploads as well as making a simple-to-use template that can be used in other projects.

To upload files with a larger threshold, one can make a zip file and then use `zipsplit` to make a few large chunks, depending on the size of your `/tmp` directory (Run `df -h /tmp` to see how much space you have available - with 8 GB available for instance one can set the zip chunks to have a size of 2GB to upload a few chunks).

`upload.js` is intended to be run with the REPL (`$node` -> `>.load upload.js` -> `>storeWithProgress(path="some/path/here")` but with few modifications you can import it as needed in your projects.

The methods are adapted from web3.storage's official docs.
