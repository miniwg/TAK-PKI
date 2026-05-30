# TAK-PKI
Updated Public Key Infrastructure scripts for TAK server to address OpenSSL 3 incompatibilities 

## Issue
OpenSSL v3 blocks the use of pkcs12 key which use RC2-40-CBC encryption.  These versions of the TAK server PKI scripts remove test which alway results in the creation of pkcs12 keys with RC2-40-CBC encryption.

These are temporary substitutes until the original TAK server scripts are updated

## Installation
Copy the files makeRootCAmwg.sh and MakeCertmwg.sh into the /opt/tak/certs folder

Set the correct ownership and permissions:
`sudo chown tak: makeRootCAmwg.sh`
`sudo chown tak: makeCertmwg.sh`
`sudo chmod 500 makeRootCAmwg.sh`
`sudo chmod 500 makeCertmwg.sh`

## Usage
Wherever the installation guide refers to makeRootCA.sh or MakeCert.sh use the *mwg.sh version above instead.
