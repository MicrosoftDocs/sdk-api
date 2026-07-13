---
UID: NS:windnsdef.DNS_NXT_DATAA
title: DNS_NXT_DATAA (windnsdef.h)
description: The DNS_NXT_DATA structure represents a DNS next (NXT) resource record (RR) as specified in section 5 of RFC 2535. (ANSI)
helpviewer_keywords: ["*PDNS_NXT_DATA","*PDNS_NXT_DATAA","DNS_NXT_DATA","DNS_NXT_DATA structure [DNS]","DNS_NXT_DATAA","PDNS_NXT_DATA","PDNS_NXT_DATA structure pointer [DNS]","_dns_dns_nxt_data","dns.dns_nxt_data","windnsdef/DNS_NXT_DATA","windnsdef/PDNS_NXT_DATA"]
old-location: dns\dns_nxt_data.htm
tech.root: DNS
ms.assetid: 0e5370c2-30d3-4bb7-85a0-f4412f5572fd
ms.date: 01/15/2025
ms.keywords: '*PDNS_NXT_DATA, *PDNS_NXT_DATAA, DNS_NXT_DATA, DNS_NXT_DATA structure [DNS], DNS_NXT_DATAA, PDNS_NXT_DATA, PDNS_NXT_DATA structure pointer [DNS], _dns_dns_nxt_data, dns.dns_nxt_data, windnsdef/DNS_NXT_DATA, windnsdef/PDNS_NXT_DATA'
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
req.typenames: DNS_NXT_DATAA, *PDNS_NXT_DATAA
req.redist: 

f1_keywords:
 - PDNS_NXT_DATAA
 - windnsdef/PDNS_NXT_DATAA
 - DNS_NXT_DATAA
 - windnsdef/DNS_NXT_DATAA
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
 - DNS_NXT_DATA
---

# DNS_NXT_DATAA structure


## -description

The 
<b>DNS_NXT_DATA</b> structure represents a DNS next (NXT) resource record (RR) as specified in section 5 of <a href="https://www.ietf.org/rfc/rfc2535.txt">RFC 2535</a>.

## -struct-fields

### -field pNameNext

A pointer to a string that represents the name of the next domain.

### -field wNumTypes

The number of elements in the <b>wTypes</b> array. <b>wNumTypes</b> must be 2 or greater but cannot exceed 8.

### -field size_is

### -field size_is.wNumTypes

### -field wTypes

A <b>BYTE</b> array that contains a bitmap which specifies the RR types that are present  in the next domain. Each bit in the array corresponds to a <a href="/windows/win32/DNS/dns-constants">DNS Record Type</a> as defined in section 5.2 of <a href="https://www.ietf.org/rfc/rfc2535.txt">RFC 2535</a>.

## -remarks

The 
<b>DNS_NXT_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.





> [!NOTE]
> The windns.h header defines DNS_NXT_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

