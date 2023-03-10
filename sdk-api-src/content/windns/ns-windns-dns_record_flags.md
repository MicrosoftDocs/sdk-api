---
UID: NS:windns._DnsRecordFlags
title: DNS_RECORD_FLAGS (windns.h)
description: The DNS_RECORD_FLAGS structure is used to set flags for use in the DNS_RECORD structure.
helpviewer_keywords: ["DNS_RECORD_FLAGS","DNS_RECORD_FLAGS structure [DNS]","_DnsRecordFlags","_dns_dns_record_flags","dns.dns_record_flags","windns/DNS_RECORD_FLAGS"]
old-location: dns\dns_record_flags.htm
tech.root: DNS
ms.assetid: 53c1c8bc-20b0-4b15-b2b6-9c9854f73ee3
ms.date: 12/05/2018
ms.keywords: DNS_RECORD_FLAGS, DNS_RECORD_FLAGS structure [DNS], _DnsRecordFlags, _dns_dns_record_flags, dns.dns_record_flags, windns/DNS_RECORD_FLAGS
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
targetos: Windows
req.typenames: DNS_RECORD_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DnsRecordFlags
 - windns/_DnsRecordFlags
 - DNS_RECORD_FLAGS
 - windns/DNS_RECORD_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_RECORD_FLAGS
---

# DNS_RECORD_FLAGS structure


## -description

The 
<b>DNS_RECORD_FLAGS</b> structure is used to set flags for use in the 
<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure.

## -struct-fields

### -field Section

A <a href="/windows/win32/api/windns/ne-windns-dns_section">DNS_SECTION</a> value that specifies the section of interest returned from the 
<a href="/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a> function call.

### -field Delete

Reserved. Do not use.

### -field CharSet

A <a href="/windows/desktop/api/windns/ne-windns-dns_charset">DNS_CHARSET</a> value that specifies the character set used in the associated function call.

### -field Unused

Reserved. Do not use.

### -field Reserved

Reserved. Do not use.

## -see-also

<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>