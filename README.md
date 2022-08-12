# OSI-Model-Lab

Recently, I was trying to understand more about the OSI models and how data travels across internal networks.
So, I decided to create a scenario using the Cisco packet tracer. My topology was a network of four computers, two servers, and a switch, all connected together. Each with its own IP address and subnet address configured. I then tried to access one of the servers from one of the computers. Here's what I found:
Two packets were created – A TCP segment and an ARP request. What exactly are these two packets, and what do they do?
On ethernet, devices communicate with what's known as a MAC address. An ARP request is used to determine the address of a server so that your computer can communicate with it.
In my scenario, my ARP request was sent to the switch. The switch then sent a broadcast message asking for the server's MAC address. All the computers on my network received the broadcast, but only the server responded with its MAC address. A connection was then established between the computer and the server.
A TCP packet contains the data that is being transferred when a connection is established between two devices. In my case, the TCP server had the web request made to the server.

Let's look at how this topology synchronized with the OSI model.
First, a connection was established between the computer and the server at the physical layer. This was typically done using an Ethernet cable. Next, we had the ARP protocol at the data-link and network layer. This handled the mapping of IP addresses to MAC addresses.
At the transport layer, we had the TCP protocol. Finally, at the application layer, we had the HTTP protocol. This allowed us to request and receive data from the server.
