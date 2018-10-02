---
UID: NS:windns.__unnamed_struct_10
title: DNS_MX_DATAA
author: windows-sdk-content
description: The DNS_MX_DATA structure represents a DNS mail exchanger (MX) record as specified in section 3.3.9 of RFC 1035.
old-location: dns\dns_mx_data.htm
tech.root: DNS
ms.assetid: 72a0b42e-a7af-42d2-b672-cf06d0b5d1ba
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDNS_MX_DATA, *PDNS_MX_DATAA, DNS_MX_DATA, DNS_MX_DATA structure [DNS], DNS_MX_DATAA, PDNS_MX_DATA, PDNS_MX_DATA structure pointer [DNS], _dns_dns_mx_data, dns.dns_mx_data, windns/DNS_MX_DATA, windns/PDNS_MX_DATA"
ms.prod: windows
ms.technology: windows-sdk
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
 - DNS_MX_DATA
product: Windows
targetos: Windows
req.typenames: DNS_MX_DATAA, *PDNS_MX_DATAA
req.redist: 
---

# DNS_MX_DATAA structure


## -description


The 
<b>DNS_MX_DATA</b> structure represents a DNS mail exchanger (MX) record as specified in section 3.3.9 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>.


## -struct-fields




### -field pNameExchange

A pointer to a string that represents the fully qualified domain name (FQDN) of the host willing to act as a mail exchange.


### -field wPreference

A preference given to this resource record among others of the same owner. Lower values are preferred.


### -field Pad

Reserved for padding. Do not use.


## -remarks



The 
<b>DNS_MX_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

