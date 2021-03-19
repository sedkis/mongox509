# MongoDB with X509 Auth

Following this guide:
https://docs.mongodb.com/manual/appendix/security/appendixA-openssl-ca/


## tl;dr:

### 1. Run Mongo With mTLS

$ mongod --config mongod.yaml

### 2. Connect to Mongo

4.2 Mongo or greater

$ mongo --tls --host tyk-mongo --tlsCertificateKeyFile test-client.pem  --tlsCAFile test-ca.pem

Otherwise

$ mongo --ssl --host tyk-mongo --sslPEMKeyFile test-client.pem  --sslCAFile test-ca.pem

