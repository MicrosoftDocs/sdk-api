---
UID: NS:windns._DnsAddr
title: DNS_ADDR (windns.h)

description: A DNS_ADDR structure stores an IPv4 or IPv6 address.
old-location: dns\dns_addr.htm
tech.root: DNS
ms.assetid: c14e6fc0-34b3-40e8-b9b8-61e4aea01677

ms.date: 12/05/2018
ms.keywords: '*PDNS_ADDR, DNS_ADDR, DNS_ADDR structure [DNS], PDNS_ADDR, PDNS_ADDR structure pointer [DNS], dns.dns_addr, windns/DNS_ADDR, windns/PDNS_ADDR'
ms.topic: struct
f1_keywords:
- windns/DNS_ADDR
dev_langs:
 - c++
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Windns.h
api_name:
- DNS_ADDR
targetos: Windows
req.typenames: DNS_ADDR, *PDNS_ADDR
req.redist: 
ms.custom: 19H1
---

# DNS_ADDR structure


## -description


A <b>DNS_ADDR</b> structure stores an IPv4 or IPv6 address.


## -struct-fields




### -field MaxSa

A value that contains the socket IP address. It is a <a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr_in</a> structure if the address is IPv4 and a sockaddr_in6 structure if the address is IPv6.


### -field DnsAddrUserDword

Reserved. Must be 0.


## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_addr_array">DNS_ADDR_ARRAY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-dns_query_result">DNS_QUERY_RESULT</a>
 

 

