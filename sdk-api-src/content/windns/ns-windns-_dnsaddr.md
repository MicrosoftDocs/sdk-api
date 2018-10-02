---
UID: NS:windns._DnsAddr
title: "_DnsAddr"
author: windows-sdk-content
description: A DNS_ADDR structure stores an IPv4 or IPv6 address.
old-location: dns\dns_addr.htm
tech.root: DNS
ms.assetid: c14e6fc0-34b3-40e8-b9b8-61e4aea01677
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDNS_ADDR, DNS_ADDR, DNS_ADDR structure [DNS], PDNS_ADDR, PDNS_ADDR structure pointer [DNS], _DnsAddr, dns.dns_addr, windns/DNS_ADDR, windns/PDNS_ADDR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: DNS_ADDR, *PDNS_ADDR
req.redist: 
---

# _DnsAddr structure


## -description


A <b>DNS_ADDR</b> structure stores an IPv4 or IPv6 address.


## -struct-fields




### -field MaxSa

A value that contains the socket IP address. It is a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr_in</a> structure if the address is IPv4 and a sockaddr_in6 structure if the address is IPv6.


### -field DnsAddrUserDword

Reserved. Must be 0.


## -see-also




<a href="https://msdn.microsoft.com/5FD7F28B-D1A6-4731-ACB9-A7BB23CC1FB4">DNS_ADDR_ARRAY</a>



<a href="https://msdn.microsoft.com/03EB1DC2-FAB0-45C5-B438-E8FFDD218F09">DNS_QUERY_RESULT</a>
 

 

