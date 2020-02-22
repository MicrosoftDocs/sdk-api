---
UID: NS:windns.__unnamed_struct_15
title: DNS_AAAA_DATA (windns.h)
description: The DNS_AAAA_DATA structure represents a DNS IPv6 (AAAA) record as specified in RFC 3596.
old-location: dns\dns_aaaa_data.htm
tech.root: DNS
ms.assetid: 0bc48e86-368c-431c-b67a-b7689dca8d3c
ms.date: 12/05/2018
ms.keywords: '*PDNS_AAAA_DATA, DNS_AAAA_DATA, DNS_AAAA_DATA structure [DNS], PDNS_AAAA_DATA, PDNS_AAAA_DATA structure pointer [DNS], _dns_dns_aaaa_data, dns.dns_aaaa_data, windns/DNS_AAAA_DATA, windns/PDNS_AAAA_DATA'
f1_keywords:
- windns/DNS_AAAA_DATA
dev_langs:
- c++
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
targetos: Windows
req.typenames: DNS_AAAA_DATA, *PDNS_AAAA_DATA
req.redist: 
ms.custom: 19H1
---

# DNS_AAAA_DATA structure


## -description


The 
<b>DNS_AAAA_DATA</b> structure represents a DNS IPv6 (AAAA) record as specified in <a href="https://www.ietf.org/rfc/rfc3596.txt">RFC 3596</a>.


## -struct-fields




### -field Ip6Address

An <a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-ip6_address">IP6_ADDRESS</a> data type that contains an IPv6 address.


## -remarks



The 
<b>DNS_AAAA_DATA</b> structure is used in conjunction with the 
<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>
 

 

