---
UID: NS:ws2ipdef._sockaddr_in6_pair
title: "_sockaddr_in6_pair"
author: windows-driver-content
description: Contains pointers to a pair of IP addresses that represent a source and destination address pair.
old-location: iphlp\sockaddr_in6_pair.htm
old-project: IpHlp
ms.assetid: 0265f8e0-8b35-4d9d-bf22-e98e9ff36a17
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PSOCKADDR_IN6_PAIR, PSOCKADDR_IN6_PAIR, PSOCKADDR_IN6_PAIR structure pointer [IP Helper], SOCKADDR_IN6_PAIR, SOCKADDR_IN6_PAIR structure [IP Helper], _sockaddr_in6_pair, iphlp.sockaddr_in6_pair, ws2ipdef/PSOCKADDR_IN6_PAIR, ws2ipdef/SOCKADDR_IN6_PAIR"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SOCKADDR_IN6_PAIR, *PSOCKADDR_IN6_PAIR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ws2ipdef.h
api_name:
-	SOCKADDR_IN6_PAIR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

