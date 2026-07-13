---
UID: NS:windnsdef.DNS_NULL_DATA
title: DNS_NULL_DATA (windnsdef.h)
description: The DNS_NULL_DATA structure represents NULL data for a DNS resource record as specified in section 3.3.10 of RFC 1035.
helpviewer_keywords: ["*PDNS_NULL_DATA","DNS_NULL_DATA","DNS_NULL_DATA structure [DNS]","PDNS_NULL_DATA","PDNS_NULL_DATA structure pointer [DNS]","_dns_dns_null_data","dns.dns_null_data","windnsdef/DNS_NULL_DATA","windnsdef/PDNS_NULL_DATA"]
old-location: dns\dns_null_data.htm
tech.root: DNS
ms.assetid: c31e468f-8efd-4173-bc2c-442ee4df737f
ms.date: 01/15/2025
ms.keywords: '*PDNS_NULL_DATA, DNS_NULL_DATA, DNS_NULL_DATA structure [DNS], PDNS_NULL_DATA, PDNS_NULL_DATA structure pointer [DNS], _dns_dns_null_data, dns.dns_null_data, windnsdef/DNS_NULL_DATA, windnsdef/PDNS_NULL_DATA'
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
req.typenames: DNS_NULL_DATA, *PDNS_NULL_DATA
req.redist: 

f1_keywords:
 - PDNS_NULL_DATA
 - windnsdef/PDNS_NULL_DATA
 - DNS_NULL_DATA
 - windnsdef/DNS_NULL_DATA
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
 - DNS_NULL_DATA
---

# DNS_NULL_DATA structure


## -description

The 
<b>DNS_NULL_DATA</b> structure represents NULL data for a DNS resource record as specified in section 3.3.10 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.

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
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

