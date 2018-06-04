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

# _sockaddr_in6_pair structure


## -description


The <b>SOCKADDR_IN6_PAIR</b> structure contains pointers to a pair of IP addresses that represent a source and destination address pair.


## -struct-fields




### -field SourceAddress

A pointer to an IP source address represented as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570824">SOCKADDR_IN6</a> structure. The address family is in host byte order and the IPv6 address, port, flow information, and zone ID are  in network byte order.


### -field DestinationAddress

A pointer to an IP source address represented as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570824">SOCKADDR_IN6</a> structure. The address family is in host byte order and the IPv6 address, port, flow information, and zone ID are  in network byte order.


## -remarks



The <b>SOCKADDR_IN6_PAIR</b> structure is defined on Windows Vista and later. 

Any IPv4 addresses in the <b>SOCKADDR_IN6_PAIR</b> structure must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node. For more information on the IPv4-mapped IPv6 address format, see <a href="https://msdn.microsoft.com/7ae49081-ffb5-4eee-b488-2541398e7acc">Dual-Stack Sockets</a>.

The <b>SOCKADDR_IN6_PAIR</b> structure is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546219">CreateSortedAddressPairs</a> function.  

Note that the <i>Ws2ipdef.h</i> header file is automatically included in <i>Ws2tcpip.h</i> header file, and should never be used directly.





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546219">CreateSortedAddressPairs</a>



<a href="https://msdn.microsoft.com/7ae49081-ffb5-4eee-b488-2541398e7acc">Dual-Stack Sockets</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>
 

 

