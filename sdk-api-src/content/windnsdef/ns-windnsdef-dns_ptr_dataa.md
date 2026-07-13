---
UID: NS:windnsdef.DNS_PTR_DATAA
title: DNS_PTR_DATAA (windnsdef.h)
description: The DNS_PTR_DATA structure represents a DNS pointer (PTR) record as specified in section 3.3.12 of RFC 1035. (ANSI)
helpviewer_keywords: ["*PDNS_PTR_DATA","*PDNS_PTR_DATAA","DNS_PTR_DATA","DNS_PTR_DATA structure [DNS]","DNS_PTR_DATAA","PDNS_PTR_DATA","PDNS_PTR_DATA structure pointer [DNS]","_dns_dns_ptr_data","dns.dns_ptr_data","windnsdef/DNS_PTR_DATA","windnsdef/PDNS_PTR_DATA"]
old-location: dns\dns_ptr_data.htm
tech.root: DNS
ms.assetid: 8b7f8898-ac91-46da-876c-889c427068a3
ms.date: 01/15/2025
ms.keywords: '*PDNS_PTR_DATA, *PDNS_PTR_DATAA, DNS_PTR_DATA, DNS_PTR_DATA structure [DNS], DNS_PTR_DATAA, PDNS_PTR_DATA, PDNS_PTR_DATA structure pointer [DNS], _dns_dns_ptr_data, dns.dns_ptr_data, windnsdef/DNS_PTR_DATA, windnsdef/PDNS_PTR_DATA'
req.header: windnsdef.h
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
targetos: Windows
req.typenames: DNS_PTR_DATAA, *PDNS_PTR_DATAA
req.redist: 

f1_keywords:
 - PDNS_PTR_DATAA
 - windnsdef/PDNS_PTR_DATAA
 - DNS_PTR_DATAA
 - windnsdef/DNS_PTR_DATAA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windnsdef.h
api_name:
 - DNS_PTR_DATA
---

# DNS_PTR_DATAA structure


## -description

The 
<b>DNS_PTR_DATA</b> structure represents a DNS pointer (PTR) record as specified in section 3.3.12 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.

## -struct-fields

### -field pNameHost

A pointer to a string that represents the pointer (PTR) record data.

## -remarks

The 
<b>DNS_PTR_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.





> [!NOTE]
> The windns.h header defines DNS_PTR_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

