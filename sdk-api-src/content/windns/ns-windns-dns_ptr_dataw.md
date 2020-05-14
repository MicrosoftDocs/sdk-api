---
UID: NS:windns.__unnamed_struct_3
title: DNS_PTR_DATAW (windns.h)
description: The DNS_PTR_DATA structure represents a DNS pointer (PTR) record as specified in section 3.3.12 of RFC 1035.
helpviewer_keywords: ["*PDNS_PTR_DATA","*PDNS_PTR_DATAW","DNS_PTR_DATA","DNS_PTR_DATA structure [DNS]","DNS_PTR_DATAW","PDNS_PTR_DATA","PDNS_PTR_DATA structure pointer [DNS]","_dns_dns_ptr_data","dns.dns_ptr_data","windns/DNS_PTR_DATA","windns/PDNS_PTR_DATA"]
old-location: dns\dns_ptr_data.htm
tech.root: DNS
ms.assetid: 8b7f8898-ac91-46da-876c-889c427068a3
ms.date: 12/05/2018
ms.keywords: '*PDNS_PTR_DATA, *PDNS_PTR_DATAW, DNS_PTR_DATA, DNS_PTR_DATA structure [DNS], DNS_PTR_DATAW, PDNS_PTR_DATA, PDNS_PTR_DATA structure pointer [DNS], _dns_dns_ptr_data, dns.dns_ptr_data, windns/DNS_PTR_DATA, windns/PDNS_PTR_DATA'
f1_keywords:
- windns/DNS_PTR_DATA
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
- DNS_PTR_DATA
targetos: Windows
req.typenames: DNS_PTR_DATAW, *PDNS_PTR_DATAW
req.redist: 
ms.custom: 19H1
---

# DNS_PTR_DATAW structure


## -description


The 
<b>DNS_PTR_DATA</b> structure represents a DNS pointer (PTR) record as specified in section 3.3.12 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.


## -struct-fields




### -field pNameHost

A pointer to a string that represents the pointer (PTR) record data.


## -remarks



The 
<b>DNS_PTR_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>
 

 

