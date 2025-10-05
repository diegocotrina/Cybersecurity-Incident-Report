# Cybersecurity-Incident-Report

**Scenario**

**Review the following scenario. Then complete the step-by-step instructions.**

You work as a security analyst for a travel agency that advertises sales and promotions on the company’s website. The employees of the company regularly access the company’s sales webpage to search for vacation packages their customers might like. 
One afternoon, you receive an automated alert from your monitoring system indicating a problem with the web server. You attempt to visit the company’s website, but you receive a connection timeout error message in your browser.
You use a packet sniffer to capture data packets in transit to and from the web server. You notice a large number of TCP SYN requests coming from an unfamiliar IP address. The web server appears to be overwhelmed by the volume of incoming traffic and is losing its ability to respond to the abnormally large number of SYN requests. You suspect the server is under attack by a malicious actor.
You take the server offline temporarily so that the machine can recover and return to a normal operating status. You also configure the company’s firewall to block the IP address that was sending the abnormal number of SYN requests. You know that your IP blocking solution won’t last long, as an attacker can spoof other IP addresses to get around this block. You need to alert your manager about this problem quickly and discuss the next steps to stop this attacker and prevent this problem from happening again. You will need to be prepared to tell your boss about the type of attack you discovered and how it was affecting the web server and employees.


**Section 1: Identify the type of attack that may have caused this network interruption**
One potential explanation for the website's connection timeout error message is: the server does not have capacity to respond to the abnormal number of SYN requests which it’s receiving.

The logs show that: the server is receiving an abnormal number of SYN requests from a specific ISIN (DoS attack) which deteriorates its work performance.

This event could be: a SYN DoS attack by a malicious agent


**Section 2: Explain how the attack is causing the website to malfunction**
When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol. Explain the three steps of the handshake:
1. First, a SYN request is made to the server

2. Once received, the server replies with the SYN ACK response

3. Lastly, an ACK request is sent back to the server and the connection is made

**Explain what happens when a malicious actor sends a large number of SYN packets all at once:** If the server does not have the capacity to handle such a high number of SYN requests, it will collapse resulting in real SYN requests made by real customers unsuccessful.

**Explain what the logs indicate and how that affects the server:** the logs indicate a massive number of SYN requests being made by a singular IP address (203.0.113.0) which very likely indicates a SYN DoS attack on the web server, resulting in its inability to attend all request and failure to form connections i.e., timeout error message on the clients’ side.

