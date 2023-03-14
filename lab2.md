## Pripremna pitanja

1. What is the _Address Resolution Protocol (ARP)_, and what is its role in a network?
    - ARP is a communication protocol from Data Link Layer which is used to map IP address to a physical adress (MAC address). It broadcastes a message to all devices on the network,
      asking them to respond what is their MAC address, while he already knows theirs IP address.
  
2. What is a _Man-in-the-Middle (MitM)_ attack, and how does ARP spoofing enable it?
   - ARP spoofing is an attack when the atacker sends its MAC address connected to the IP address of another device in the network to the device which is broadacsting
     a message in which it asks for all the MAC addresses of devices in its network. MitM is an attack in which attacker device intercepts messages exchanged between
     two devices, and does something with them (read/change/append data). Using ARP spoofing, MitM attack can steal data which are meant for some other device.

3. How does an attacker use ARP spoofing to intercept network traffic?
   - It deceives the broadcasting device that it represents the other device in the network with some other IP address and instead of that other device, 
     it sends its own MAC address. He intercepts all data being send to original IP address with which it is deceiveing the victim. 
  
4. How is the _cookie_ used to derive the encryption/decryption key?
   - We use secret cookie to derive encryption and decryption key. We derive this cookie using the derive function in code.

5. What REST API request do you need to send to the _crypto oracle_ the secret cookie?
   - GET /arp/cookie
  
6. How do you obtain the authentication token?
   - You ask for it from oracle crypto server while authenticating yourself using your username and password 
  
7. How do you use the authentication token to obtain the cookie?
   - When we are authenticated we can obtain the cookie because the oracle crypto server knows to whom its sending the cookie when we request it using GET request.

8. What encryption mode is used to encrypt the challenge in this lab?
   - AES-CBC (AES cipher and CBC encryption)

9. What tool can you use to capture network traffic on a local network interface?
    - tcpdump
