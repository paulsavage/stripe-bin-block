# stripe-bin-block

## About
This is a quick list of of rule blocking for credit cards based on BINs. The BIN (_Bank Identification Number_) is the numbers at the start of the card, generally the first 6 digits, e.g. `464088` . If you are having a particular issue with a certain credit card issuer, with respect to fraud, chargebacks, etc. it is possible to block these BINs. In our case we see virtual cards are generally abused and we needed a way to block these. 
## Virtual cards 
Virtual cards allow you generate new full credit card numbers on the fly. While there are privacy advantages they are also open to abuse, i.e. people who you've blocked from using your services 
# Finding BIN Lists 
It can be hard to find good lists of BINs, they change often and banks don't share them so openly. Curretly our go to is 
* https://binov.net/  ~ Bank to BIN list 
* https://binlist.net/ ~ BIN Lookup 
* https://www.bankbinlist.com/ - Country BIN list 
## Format
I've share a number of files based on the card issuer. These are named based on the company name and series number. `BANKNAME`-`SERIES`.txt, e.g. `revolut-02.txt`  
## Disclaimer
Use at your own risk. You can use these to trigger an outright block, or you can flag these transactions for reviews. 

## Notes 
* Stripe Rules can only be `1,000` character
* Have a list you'd like to share, please share with a pull request
* In the case that a bank may have multiple operating names we've used the most familar version. 

## Webhooks
It is also possible to block users who user a previously bad credit card. More about that soon. 
