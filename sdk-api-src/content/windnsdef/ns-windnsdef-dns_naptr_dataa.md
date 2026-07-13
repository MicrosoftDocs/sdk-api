---
UID: NS:windnsdef.DNS_NAPTR_DATAA
title: DNS_NAPTR_DATAA (windnsdef.h)
description: The DNS_NAPTR_DATA structure represents a Naming Authority Pointer (NAPTR) DNS Resource Record (RR) as specified in RFC 2915. (ANSI)
helpviewer_keywords: ["*PDNS_NAPTR_DATA","*PDNS_NAPTR_DATAA","DNS_NAPTR_DATA","DNS_NAPTR_DATA structure [DNS]","DNS_NAPTR_DATAA","PDNS_NAPTR_DATA","PDNS_NAPTR_DATA structure pointer [DNS]","dns.dns_naptr_data","windnsdef/DNS_NAPTR_DATA","windnsdef/PDNS_NAPTR_DATA"]
old-location: dns\dns_naptr_data.htm
tech.root: DNS
ms.assetid: 8f576efb-4ef3-4fc0-8cf5-d373460a3b3c
ms.date: 01/15/2025
ms.keywords: '*PDNS_NAPTR_DATA, *PDNS_NAPTR_DATAA, DNS_NAPTR_DATA, DNS_NAPTR_DATA structure [DNS], DNS_NAPTR_DATAA, PDNS_NAPTR_DATA, PDNS_NAPTR_DATA structure pointer [DNS], dns.dns_naptr_data, windnsdef/DNS_NAPTR_DATA, windnsdef/PDNS_NAPTR_DATA'
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
req.typenames: DNS_NAPTR_DATAA, *PDNS_NAPTR_DATAA
req.redist: 

f1_keywords:
 - PDNS_NAPTR_DATAA
 - windnsdef/PDNS_NAPTR_DATAA
 - DNS_NAPTR_DATAA
 - windnsdef/DNS_NAPTR_DATAA
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
 - DNS_NAPTR_DATA
---

# DNS_NAPTR_DATAA structure


## -description

The 
<b>DNS_NAPTR_DATA</b> structure represents a Naming Authority Pointer (NAPTR) DNS Resource Record (RR) as specified in <a href="https://www.ietf.org/rfc/rfc2915.txt">RFC 2915</a>.

## -struct-fields

### -field wOrder

 A value that determines the NAPTR RR processing order as defined in section 2 of <a href="https://www.ietf.org/rfc/rfc2915.txt">RFC 2915</a>.

### -field wPreference

A value that determines the NAPTR RR processing  order  for records with the same <b>wOrder</b> value as defined in section 2 of <a href="https://www.ietf.org/rfc/rfc2915.txt">RFC 2915</a>.

### -field pFlags

A pointer to a string  that represents a set of NAPTR RR flags which determine the interpretation and processing of NAPTR record fields as defined in section 2 of <a href="https://www.ietf.org/rfc/rfc2915.txt">RFC 2915</a>.

### -field pService

A pointer to a string that represents the available services in this rewrite path as defined in section 2 of <a href="https://www.ietf.org/rfc/rfc2915.txt">RFC 2915</a>.

### -field pRegularExpression

A pointer to a string that represents a substitution expression as defined in sections 2 and 3 of <a href="https://www.ietf.org/rfc/rfc2915.txt">RFC 2915</a>.

### -field pReplacement

A pointer to a string that represents the next NAPTR query name as defined in section 2 of <a href="https://www.ietf.org/rfc/rfc2915.txt">RFC 2915</a>.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

## -remarks

> [!NOTE]
> The windns.h header defines DNS_NAPTR_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

