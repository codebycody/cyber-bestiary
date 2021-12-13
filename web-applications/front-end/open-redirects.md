# Open Redirect
---
## Description
Open Redirect vulnerabilities occur when a target visits a website and that website redirects the browser to a different URL. Open redirect exploits the trust a given domain holds to lure targets to a malicious website
An http parameter may contain a URL value and could cause the web application to redirect the request to the specified URL. By modifying the URL value to a malicious site, an attacker may successfully launch a phishing scam and steal user credentials. Because the server name in the modified link is identical to the original site, phishing attempts have a more trustworthy appearance.

## Alternate Terms
- URL Redirection
- Cross-site Redirect
- Cross-domain Redirect

## Explanation

## CVSS
[6.1](CVSS:3.0/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N)
## Impact Exploitability
[Impact: 2.7](CVSS:3.0/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N)
[Exploitability: 2.8](CVSS:3.0/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N)
## Detection

## Remediation(s)
There are several ways to avoid open redirect vulnerabilities. Here are key methods recommended by the Open Web Application Security Project (OWASP):
- Do not use forwards and redirects.
-Do not allow URLs as user input for a destination.
- If absolutely necessary to accept a URL from users, ask the users to provide a short name, token, or ID that is mapped server-side to the full target URL. This method provides a high level of protection against attacks that tamper with URLs. However, you must be careful not to introduce an enumeration vulnerability that allows users to cycle through IDs and find all possible redirect targets.
- When user input cannot be avoided, you should make sure that all supplied values are valid, are appropriate for the application, and are authorized for each user.
- Create a list of all trusted URLs, including hosts or a regex, in order to sanitize input. Prefer to use an allow-list approach when creating this list, instead of a block list.
- Force redirects to first go to a page that notify users they are redirected out of the website. The message should clearly display the destination and ask users to click on a link to confirm that they want to move to the new destination.

## Case Study(s)
