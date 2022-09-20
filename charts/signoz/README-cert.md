sudo certbot -d *.signoz.io --manual --preferred-challenges dns certonly

NEXT STEPS:
- This certificate will not be renewed automatically. Autorenewal of --manual certificates requires the use of an authentication hook script (--manual-auth-hook) but one was not provided. To renew this certificate, repeat this same certbot command before the certificate's expiry date.




kubectl -n <customer-namespace> create secret generic signoz-io-ssl --from-file=./signoz-io-pem-files/fullchain.pem --from-file=./signoz-io-pem-files/privkey.pem
