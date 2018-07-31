---
UID: NS:windns.__unnamed_struct_29
title: DNS_NXT_DATAA
author: windows-sdk-content
description: The DNS_NXT_DATA structure represents a DNS next (NXT) resource record (RR) as specified in section 5 of RFC 2535.
old-location: dns\dns_nxt_data.htm
old-project: DNS
ms.assetid: 0e5370c2-30d3-4bb7-85a0-f4412f5572fd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PDNS_NXT_DATA, *PDNS_NXT_DATAA, DNS_NXT_DATA, DNS_NXT_DATA structure [DNS], DNS_NXT_DATAA, PDNS_NXT_DATA, PDNS_NXT_DATA structure pointer [DNS], _dns_dns_nxt_data, dns.dns_nxt_data, windns/DNS_NXT_DATA, windns/PDNS_NXT_DATA"
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
tech.root: 
req.typenames: DNS_NXT_DATAA, *PDNS_NXT_DATAA
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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

A <b>BYTE</b> array that contains a bitmap which specifies the RR types that are present  in the next domain. Each bit in the array corresponds to a <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Record Type</a> as defined in section 5.2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=124775">RFC 2535</a>.


## -remarks



The 
<b>DNS_NXT_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

