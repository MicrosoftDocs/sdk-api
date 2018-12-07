---
UID: NS:windns.__unnamed_struct_15
title: DNS_AAAA_DATA
author: windows-sdk-content
description: The DNS_AAAA_DATA structure represents a DNS IPv6 (AAAA) record as specified in RFC 3596.
old-location: dns\dns_aaaa_data.htm
tech.root: dns
ms.assetid: 0bc48e86-368c-431c-b67a-b7689dca8d3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDNS_AAAA_DATA, DNS_AAAA_DATA, DNS_AAAA_DATA structure [DNS], PDNS_AAAA_DATA, PDNS_AAAA_DATA structure pointer [DNS], _dns_dns_aaaa_data, dns.dns_aaaa_data, windns/DNS_AAAA_DATA, windns/PDNS_AAAA_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - DNS_AAAA_DATA
product: Windows
targetos: Windows
req.typenames: DNS_AAAA_DATA, *PDNS_AAAA_DATA
req.redist: 
---

# DNS_AAAA_DATA structure


## -description


The 
<b>DNS_AAAA_DATA</b> structure represents a DNS IPv6 (AAAA) record as specified in <a href="http://go.microsoft.com/fwlink/p/?linkid=107027">RFC 3596</a>.


## -struct-fields




### -field Ip6Address

An <a href="https://msdn.microsoft.com/789400be-03c7-4c4f-9e78-fa2573cf114d">IP6_ADDRESS</a> data type that contains an IPv6 address.


## -remarks



The 
<b>DNS_AAAA_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

