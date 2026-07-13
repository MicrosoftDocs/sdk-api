---
UID: NS:windnsdef.DNS_MX_DATAA
title: DNS_MX_DATAA (windnsdef.h)
description: The DNS_MX_DATA structure represents a DNS mail exchanger (MX) record as specified in section 3.3.9 of RFC 1035. (ANSI)
helpviewer_keywords: ["*PDNS_MX_DATA","*PDNS_MX_DATAA","DNS_MX_DATA","DNS_MX_DATA structure [DNS]","DNS_MX_DATAA","PDNS_MX_DATA","PDNS_MX_DATA structure pointer [DNS]","_dns_dns_mx_data","dns.dns_mx_data","windnsdef/DNS_MX_DATA","windnsdef/PDNS_MX_DATA"]
old-location: dns\dns_mx_data.htm
tech.root: DNS
ms.assetid: 72a0b42e-a7af-42d2-b672-cf06d0b5d1ba
ms.date: 01/15/2025
ms.keywords: '*PDNS_MX_DATA, *PDNS_MX_DATAA, DNS_MX_DATA, DNS_MX_DATA structure [DNS], DNS_MX_DATAA, PDNS_MX_DATA, PDNS_MX_DATA structure pointer [DNS], _dns_dns_mx_data, dns.dns_mx_data, windnsdef/DNS_MX_DATA, windnsdef/PDNS_MX_DATA'
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
req.typenames: DNS_MX_DATAA, *PDNS_MX_DATAA
req.redist: 

f1_keywords:
 - PDNS_MX_DATAA
 - windnsdef/PDNS_MX_DATAA
 - DNS_MX_DATAA
 - windnsdef/DNS_MX_DATAA
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
 - DNS_MX_DATA
---

# DNS_MX_DATAA structure


## -description

The 
<b>DNS_MX_DATA</b> structure represents a DNS mail exchanger (MX) record as specified in section 3.3.9 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.

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
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.





> [!NOTE]
> The windns.h header defines DNS_MX_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

