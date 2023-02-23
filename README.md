# CRSBF
Custom Record Subdomain Brute Foce, Brute Force subdomains with a list of custom DNS records.

# Came from different idea
I have used other subdomain brute forcing tools, many of them are looking for subdomains with only A record, I know you can specify custom dns records with massdns, but with this script you can automate the whole thing.

# Read it before usage
There's already a list of dns records in the directory, you can add or remove dns records to the file, you need a subdomains wordlist and the tool will compile it to the targets domain itself, I use only 1.1.1.1 & 8.8.8.8 as resolver in the resolvers.txt file, you can add more resolvers dns if you want but it works fine.

# Usage
Remember that you need to install massdns first: https://github.com/blechschmidt/massdns

`chmod +x crsbf`
`./crsbf subdomains-wordlist.txt target.com`

All outputs will be saved to `target.com` directory, you can find all live subdomains at `target.com/target.com-massdns-live-subdomains.txt`.

Try this if you want to extract only subdomains from live subdomains out put:

`grep 'target.com. ' target.com-massdns-live-subdomains.txt | awk -F'. ' '{print $1}' | sort -u`

Wish you good finding.
