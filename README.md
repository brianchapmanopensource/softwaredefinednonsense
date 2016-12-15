# Software Defined Nonsense
When you need to debug IPSec transport mode (IPv4) on an ancient NetScreen FW without disrupting the IPv6 traffic on your internet connection, what do you do? Any normal person would leave this one alone, instead I split out ARP, IP proto 50 and 51, and UDP 500 using userspace TAP/TUN interface, do some MAC-nat to keep my ISP from getting confused and bridge the TAP interfaces under promisc mode.

OpenFlow would have been great, however Northbridge Zodiac units ship from Australia, and most other OF-capable switches are outside the budget of this project.

So yeah, if you'd like a nutty ethernet sort-of transparent bridge type thingy, clone this project and mess around w/ it.
