---
UID: NS:windns.__unnamed_struct_13
title: DNS_NULL_DATA
author: windows-sdk-content
description: The DNS_NULL_DATA structure represents NULL data for a DNS resource record as specified in section 3.3.10 of RFC 1035.
old-location: dns\dns_null_data.htm
tech.root: DNS
ms.assetid: c31e468f-8efd-4173-bc2c-442ee4df737f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PDNS_NULL_DATA, DNS_NULL_DATA, DNS_NULL_DATA structure [DNS], PDNS_NULL_DATA, PDNS_NULL_DATA structure pointer [DNS], _dns_dns_null_data, dns.dns_null_data, windns/DNS_NULL_DATA, windns/PDNS_NULL_DATA"
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
 - DNS_NULL_DATA
product: Windows
targetos: Windows
req.typenames: DNS_NULL_DATA, *PDNS_NULL_DATA
req.redist: 
---

# DNS_NULL_DATA structure


## -description


The 
<b>DNS_NULL_DATA</b> structure represents NULL data for a DNS resource record as specified in section 3.3.10 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>.


## -struct-fields




### -field dwByteCount

The number of bytes represented in <b>Data</b>.


### -field size_is

 


### -field size_is.dwByteCount

 


### -field Data

Null data.


## -remarks



The 
<b>DNS_NULL_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

