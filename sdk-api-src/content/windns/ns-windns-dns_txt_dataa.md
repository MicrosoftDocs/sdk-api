---
UID: NS:windns.__unnamed_struct_12
title: DNS_TXT_DATAA (windns.h)
description: The DNS_TXT_DATA structure represents a DNS text (TXT) record as specified in section 3.3.14 of RFC 1035.
helpviewer_keywords: ["*PDNS_TXT_DATA","*PDNS_TXT_DATAA","DNS_TXT_DATA","DNS_TXT_DATA structure [DNS]","DNS_TXT_DATAA","PDNS_TXT_DATA","PDNS_TXT_DATA structure pointer [DNS]","_dns_dns_txt_data","dns.dns_txt_data","windns/DNS_TXT_DATA","windns/PDNS_TXT_DATA"]
old-location: dns\dns_txt_data.htm
tech.root: DNS
ms.assetid: 3ff643e2-d736-45d5-8cf8-ab5e63caf44b
ms.date: 12/05/2018
ms.keywords: '*PDNS_TXT_DATA, *PDNS_TXT_DATAA, DNS_TXT_DATA, DNS_TXT_DATA structure [DNS], DNS_TXT_DATAA, PDNS_TXT_DATA, PDNS_TXT_DATA structure pointer [DNS], _dns_dns_txt_data, dns.dns_txt_data, windns/DNS_TXT_DATA, windns/PDNS_TXT_DATA'
f1_keywords:
- windns/DNS_TXT_DATA
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
- DNS_TXT_DATA
targetos: Windows
req.typenames: DNS_TXT_DATAA, *PDNS_TXT_DATAA
req.redist: 
ms.custom: 19H1
---

# DNS_TXT_DATAA structure


## -description


The 
<b>DNS_TXT_DATA</b> structure represents a DNS text (TXT) record as specified in section 3.3.14 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.


## -struct-fields




### -field dwStringCount

The number of strings represented in <b>pStringArray</b>.


### -field size_is

 


### -field size_is.dwStringCount

 


### -field pStringArray

An array of strings representing the descriptive text of the TXT resource record.


## -remarks



The 
<b>DNS_TXT_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>
 

 

