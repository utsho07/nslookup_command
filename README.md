# nslookup_command
First of all we need to know what is nslookup. it is a small but very powerful network administration command-line software. It has a simple interface, but it is useful.

For linux we can use below comand for install :

*`sudo apt-get update`*

*`sudo apt-get install dnsutils`*

****syntax→**** *`nslookup [-option] [name | -] [server]`*

some useful commands of nslookup:

**1) To find A record:**

`nslookup [example.com](http://example.com/)`

**2) To find NS server(name server)**

A nameserver is **a server that translates domain names into IP addresses**. It acts as a bridge between domain names, which humans can remember.

`nslookup -type=ns name.com`

****3) To query the SOA record****

The SOA(start of authority) record contains important information about a domain and who is responsible for it.

`nslookup -type=soa example.com`

****4) To find the MX records****

MX record, also known as Mail eXchanger, is a type of DNS (Domain Name System) record that specifies which mail server is responsible for receiving email messages on behalf of a domain.

`nslookup -query=mx [example.com](http://example.com/)`

****5) to find all of the available DNS records****

`nslookup -type=any name.com`

**6) To check specific DNS server:**

Apart from checking DNS records, you can use the Nslookup to review a particular DNS server and how it works.

`nslookup somewhere.com some.dns.server`

**7) Reverse DNS lookup**

`nslookup 1.2.3.4`

**8) To check for a PTR record**

You can verify if an IP address belongs to a domain name by performing a reverse DNS query.

`nslookup -type=ptr 96.96.136.185.in-addr.arpa`

online→ https://www.nslookup.io/ptr-lookup/

**9)Timeout interval:**

You can manually choose the timeout time in seconds. You can increase it to give more time for the server to respond. You can also shorter it to see which servers can respond quicker.

`nslookup -timeout=20 example.com`

**10) To enable debug mode**

`nslookup -debug website.com`
