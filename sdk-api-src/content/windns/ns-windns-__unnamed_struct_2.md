---
UID: NS:windns.__unnamed_struct_2
title: DNS_A_DATA
author: windows-sdk-content
description: The DNS_A_DATA structure represents a DNS address (A) record as specified in section 3.4.1 of RFC 1035.
old-location: dns\dns_a_data.htm
tech.root: DNS
ms.assetid: 0fd21930-1319-4ae7-b46f-2b744f4faae9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PDNS_A_DATA, DNS_A_DATA, DNS_A_DATA structure [DNS], PDNS_A_DATA, PDNS_A_DATA structure pointer [DNS], _dns_dns_a_data, dns.dns_a_data, windns/DNS_A_DATA, windns/PDNS_A_DATA"
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
 - DNS_A_DATA
product: Windows
targetos: Windows
req.typenames: DNS_A_DATA, *PDNS_A_DATA
req.redist: 
---

# DNS_A_DATA structure


## -description


The 
<b>DNS_A_DATA</b> structure represents a DNS address (A) record as specified in section 3.4.1 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>.


## -struct-fields




### -field IpAddress

An <a href="https://msdn.microsoft.com/652012a5-e45d-4ea6-896a-17e8b1ed4a05">IP4_ADDRESS</a> data type that contains an IPv4 address.


## -remarks



The 
<b>DNS_A_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

