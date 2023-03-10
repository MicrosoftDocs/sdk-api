---
UID: NS:windns.DNS_A_DATA
title: DNS_A_DATA (windns.h)
description: The DNS_A_DATA structure represents a DNS address (A) record as specified in section 3.4.1 of RFC 1035.
helpviewer_keywords: ["*PDNS_A_DATA","DNS_A_DATA","DNS_A_DATA structure [DNS]","PDNS_A_DATA","PDNS_A_DATA structure pointer [DNS]","_dns_dns_a_data","dns.dns_a_data","windns/DNS_A_DATA","windns/PDNS_A_DATA"]
old-location: dns\dns_a_data.htm
tech.root: DNS
ms.assetid: 0fd21930-1319-4ae7-b46f-2b744f4faae9
ms.date: 12/05/2018
ms.keywords: '*PDNS_A_DATA, DNS_A_DATA, DNS_A_DATA structure [DNS], PDNS_A_DATA, PDNS_A_DATA structure pointer [DNS], _dns_dns_a_data, dns.dns_a_data, windns/DNS_A_DATA, windns/PDNS_A_DATA'
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
req.typenames: DNS_A_DATA, *PDNS_A_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDNS_A_DATA
 - windns/PDNS_A_DATA
 - DNS_A_DATA
 - windns/DNS_A_DATA
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
 - DNS_A_DATA
---

# DNS_A_DATA structure


## -description

The 
<b>DNS_A_DATA</b> structure represents a DNS address (A) record as specified in section 3.4.1 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.

## -struct-fields

### -field IpAddress

An <a href="/windows/desktop/DNS/dns-data-types">IP4_ADDRESS</a> data type that contains an IPv4 address.

## -remarks

The 
<b>DNS_A_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.

## -see-also

<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>

