---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# in_pktinfo structure


## -description



			The 
<b>in_pktinfo</b> structure is used to store received packet address information, and is used by Windows to return information about received packets and also allows specifying the local IPv4 address to use for sending packets.


## -struct-fields




### -field ipi_addr

The destination IPv4 address from the IP header of the received packet when used with the <a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a>
		 function. The local source IPv4 address to set in the IP header when used with the <a href="https://msdn.microsoft.com/3b2ba645-6a70-4ba2-b4a2-5bde0c7f8d08">WSASendMsg</a> function.


### -field ipi_ifindex

The interface on which the packet was received when used with the <a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a>
		 function. The interface on which the packet should be sent  when used with the <a href="https://msdn.microsoft.com/3b2ba645-6a70-4ba2-b4a2-5bde0c7f8d08">WSASendMsg</a> function.


## -remarks



If the <a href="https://msdn.microsoft.com/C6246899-0220-4F88-B43B-CED1B1FF7DC3">IP_PKTINFO</a> socket option is set on a socket of type <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>, one of the control data objects returned by the <a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a>
		 function will contain an 
<b>in_pktinfo</b> structure used to store received packet address information.

On an IPv4  socket of type  <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>, an application can specific  the local IP address to use for sending with the <a href="https://msdn.microsoft.com/3b2ba645-6a70-4ba2-b4a2-5bde0c7f8d08">WSASendMsg</a> function. One of the control data objects passed in the <a href="https://msdn.microsoft.com/105a6e2c-1edf-4ec0-a1c2-ac0bcafeda30">WSAMSG</a> structure to the <b>WSASendMsg</b> function may contain an 
<b>in_pktinfo</b> structure used to specify the local IPv4 address to use for sending.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>in_pktinfo</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The  <i>Ws2ipdef.h</i>  header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/7ae49081-ffb5-4eee-b488-2541398e7acc">Dual-Stack Sockets for IPv6 Winsock Applications</a>



<a href="https://msdn.microsoft.com/6b06a29e-59cd-4446-bd2f-131dc25bf571">IPPROTO_IP Socket Options</a>



<a href="https://msdn.microsoft.com/7BF17538-BE92-44FE-BA3C-6B44F61D478A">IPV6_PKTINFO</a>



<a href="https://msdn.microsoft.com/C6246899-0220-4F88-B43B-CED1B1FF7DC3">IP_PKTINFO</a>



<a href="https://msdn.microsoft.com/105a6e2c-1edf-4ec0-a1c2-ac0bcafeda30">WSAMSG</a>



<a href="https://msdn.microsoft.com/a46449f7-3206-45e9-9df0-f272b8cdcc4b">WSARecvMsg</a>



<a href="https://msdn.microsoft.com/3b2ba645-6a70-4ba2-b4a2-5bde0c7f8d08">WSASendMsg</a>



<a href="https://msdn.microsoft.com/d0f1006c-2b6f-4bc9-855b-e268c27f6ca2">in6_pktinfo</a>
 

 

