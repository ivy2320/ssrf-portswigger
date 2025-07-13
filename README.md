# 🔎 SSRF with Whitelist-Based Input Filter (PortSwigger Lab)

## 🧠 Lab Summary
The lab had a basic SSRF vulnerability, but the server used a whitelist to only allow requests to `stock.weliketoshop.net`.

## 🎯 Objective
Exploit SSRF to read `/admin` on the internal server and delete a user.
1. intercepted request  using burp
   
3. Attempted SSRF using payloads
   
4. Bypassed domain whitelist using
   
4.Got a 200 OK and admin page loaded.

Sent final payload to delete user

-----
Server-Side Request Forgery (SSRF) is a powerful vulnerability that allows attackers to force a server to make arbitrary HTTP requests on their behalf. But modern applications often defend against this using domain whitelisting — only allowing requests to “safe” domains.



But what if that whitelist can be tricked?

solving portswigger labs helped me understand :

🔐 What domain-based whitelisting looks like

🧠 How to detect if a whitelist is being used

🛠️ Real-world techniques to bypass it using clever tricks





🚨 The Problem with Whitelists: Bad Validation

Most whitelists fail because developers:

Check for substrings instead of exact domains

Only block raw characters (like @, #) without decoding

Don’t normalize the URL properly

Trust DNS without realizing it’s attacker-controlled



🛠️ SSRF Whitelist Bypass Techniques include :

🧬 URL Encoding

 🪤 Subdomain Tricks

📌 Username Injection

🧨 DNS Rebinding 




resources : portSwigger Academy
