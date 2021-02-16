---
UID: NS:ws2ipdef._sockaddr_in6_pair
title: SOCKADDR_IN6_PAIR (ws2ipdef.h)
description: Contains pointers to a pair of IP addresses that represent a source and destination address pair.
helpviewer_keywords: ["*PSOCKADDR_IN6_PAIR","PSOCKADDR_IN6_PAIR","PSOCKADDR_IN6_PAIR structure pointer [IP Helper]","SOCKADDR_IN6_PAIR","SOCKADDR_IN6_PAIR structure [IP Helper]","iphlp.sockaddr_in6_pair","ws2ipdef/PSOCKADDR_IN6_PAIR","ws2ipdef/SOCKADDR_IN6_PAIR"]
old-location: iphlp\sockaddr_in6_pair.htm
tech.root: IpHlp
ms.assetid: 0265f8e0-8b35-4d9d-bf22-e98e9ff36a17
ms.date: 12/05/2018
ms.keywords: '*PSOCKADDR_IN6_PAIR, PSOCKADDR_IN6_PAIR, PSOCKADDR_IN6_PAIR structure pointer [IP Helper], SOCKADDR_IN6_PAIR, SOCKADDR_IN6_PAIR structure [IP Helper], iphlp.sockaddr_in6_pair, ws2ipdef/PSOCKADDR_IN6_PAIR, ws2ipdef/SOCKADDR_IN6_PAIR'
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SOCKADDR_IN6_PAIR, *PSOCKADDR_IN6_PAIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _sockaddr_in6_pair
 - ws2ipdef/_sockaddr_in6_pair
 - PSOCKADDR_IN6_PAIR
 - ws2ipdef/PSOCKADDR_IN6_PAIR
 - SOCKADDR_IN6_PAIR
 - ws2ipdef/SOCKADDR_IN6_PAIR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2ipdef.h
api_name:
 - SOCKADDR_IN6_PAIR
---

# SOCKADDR_IN6_PAIR structure


## -description

The <b>SOCKADDR_IN6_PAIR</b> structure contains pointers to a pair of IP addresses that represent a source and destination address pair.

## -struct-fields

### -field SourceAddress

A pointer to an IP source address represented as a <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR_IN6</a> structure. The address family is in host byte order and the IPv6 address, port, flow information, and zone ID are  in network byte order.

### -field DestinationAddress

A pointer to an IP source address represented as a <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR_IN6</a> structure. The address family is in host byte order and the IPv6 address, port, flow information, and zone ID are  in network byte order.

## -remarks

The <b>SOCKADDR_IN6_PAIR</b> structure is defined on Windows Vista and later. 

Any IPv4 addresses in the <b>SOCKADDR_IN6_PAIR</b> structure must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node. For more information on the IPv4-mapped IPv6 address format, see <a href="/windows/desktop/WinSock/dual-stack-sockets">Dual-Stack Sockets</a>.

The <b>SOCKADDR_IN6_PAIR</b> structure is used by the <a href="/windows/desktop/api/netioapi/nf-netioapi-createsortedaddresspairs">CreateSortedAddressPairs</a> function.  

Note that the <i>Ws2ipdef.h</i> header file is automatically included in <i>Ws2tcpip.h</i> header file, and should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createsortedaddresspairs">CreateSortedAddressPairs</a>



<a href="/windows/desktop/WinSock/dual-stack-sockets">Dual-Stack Sockets</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>