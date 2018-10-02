---
UID: NS:windns.__unnamed_struct_4
title: DNS_PTR_DATAA
author: windows-sdk-content
description: The DNS_PTR_DATA structure represents a DNS pointer (PTR) record as specified in section 3.3.12 of RFC 1035.
old-location: dns\dns_ptr_data.htm
tech.root: DNS
ms.assetid: 8b7f8898-ac91-46da-876c-889c427068a3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDNS_PTR_DATA, *PDNS_PTR_DATAA, DNS_PTR_DATA, DNS_PTR_DATA structure [DNS], DNS_PTR_DATAA, PDNS_PTR_DATA, PDNS_PTR_DATA structure pointer [DNS], _dns_dns_ptr_data, dns.dns_ptr_data, windns/DNS_PTR_DATA, windns/PDNS_PTR_DATA"
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
 - DNS_PTR_DATA
product: Windows
targetos: Windows
req.typenames: DNS_PTR_DATAA, *PDNS_PTR_DATAA
req.redist: 
---

# DNS_PTR_DATAA structure


## -description


The 
<b>DNS_PTR_DATA</b> structure represents a DNS pointer (PTR) record as specified in section 3.3.12 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>.


## -struct-fields




### -field pNameHost

A pointer to a string that represents the pointer (PTR) record data.


## -remarks



The 
<b>DNS_PTR_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

