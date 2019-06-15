---
UID: NS:windns.__unnamed_struct_29
title: DNS_NXT_DATAA (windns.h)
author: windows-sdk-content
description: The DNS_NXT_DATA structure represents a DNS next (NXT) resource record (RR) as specified in section 5 of RFC 2535.
old-location: dns\dns_nxt_data.htm
tech.root: DNS
ms.assetid: 0e5370c2-30d3-4bb7-85a0-f4412f5572fd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDNS_NXT_DATA, *PDNS_NXT_DATAA, DNS_NXT_DATA, DNS_NXT_DATA structure [DNS], DNS_NXT_DATAA, PDNS_NXT_DATA, PDNS_NXT_DATA structure pointer [DNS], _dns_dns_nxt_data, dns.dns_nxt_data, windns/DNS_NXT_DATA, windns/PDNS_NXT_DATA"
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
 - DNS_NXT_DATA
product: Windows
targetos: Windows
req.typenames: DNS_NXT_DATAA, *PDNS_NXT_DATAA
req.redist: 
ms.custom: 19H1
---

# DNS_NXT_DATAA structure


## -description


The 
<b>DNS_NXT_DATA</b> structure represents a DNS next (NXT) resource record (RR) as specified in section 5 of <a href="http://go.microsoft.com/fwlink/p/?linkid=124775">RFC 2535</a>.


## -struct-fields




### -field pNameNext

A pointer to a string that represents the name of the next domain.


### -field wNumTypes

The number of elements in the <b>wTypes</b> array. <b>wNumTypes</b> must be 2 or greater but cannot exceed 8.


### -field size_is

 


### -field size_is.wNumTypes

 


### -field wTypes

A <b>BYTE</b> array that contains a bitmap which specifies the RR types that are present  in the next domain. Each bit in the array corresponds to a <a href="https://docs.microsoft.com/windows/desktop/DNS/dns-constants">DNS Record Type</a> as defined in section 5.2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=124775">RFC 2535</a>.


## -remarks



The 
<b>DNS_NXT_DATA</b> structure is used in conjunction with the 
<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-_dnsrecorda">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-_dnsrecorda">DNS_RECORD</a>
 

 

