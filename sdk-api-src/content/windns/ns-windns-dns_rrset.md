---
UID: NS:windns._DnsRRSet
title: DNS_RRSET (windns.h)
description: The DNS_RRSET structure contains information about a DNS Resource Record (RR) set.
helpviewer_keywords: ["*PDNS_RRSET","*PDNS_RRSET structure [DNS]","DNS_RRSET","DNS_RRSET structure [DNS]","dns.dns_rrset","windns/*PDNS_RRSET","windns/DNS_RRSET"]
old-location: dns\dns_rrset.htm
tech.root: DNS
ms.assetid: bd87a8db-ca27-490b-85f4-912297b77a2b
ms.date: 12/05/2018
ms.keywords: '*PDNS_RRSET, *PDNS_RRSET structure [DNS], DNS_RRSET, DNS_RRSET structure [DNS], dns.dns_rrset, windns/*PDNS_RRSET, windns/DNS_RRSET'
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
req.typenames: DNS_RRSET, *PDNS_RRSET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DnsRRSet
 - windns/_DnsRRSet
 - PDNS_RRSET
 - windns/PDNS_RRSET
 - DNS_RRSET
 - windns/DNS_RRSET
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
 - DNS_RRSET
---

# DNS_RRSET structure


## -description

The <b>DNS_RRSET</b> structure contains information about a DNS Resource Record (RR) set.

## -struct-fields

### -field pFirstRR

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the first DNS RR in the set.

### -field pLastRR

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the last DNS RR in the set.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

