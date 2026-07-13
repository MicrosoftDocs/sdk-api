---
UID: NS:windnsdef.DNS_SOA_DATAW
title: DNS_SOA_DATAW (windnsdef.h)
description: The DNS_SOA_DATA structure represents a DNS start of authority (SOA) record as specified in section 3.3.13 of RFC 1035. (Unicode)
helpviewer_keywords: ["*PDNS_SOA_DATA","*PDNS_SOA_DATAW","DNS_SOA_DATA","DNS_SOA_DATA structure [DNS]","DNS_SOA_DATAW","PDNS_SOA_DATA","PDNS_SOA_DATA structure pointer [DNS]","_dns_dns_soa_data","dns.dns_soa_data","windnsdef/DNS_SOA_DATA","windnsdef/PDNS_SOA_DATA"]
old-location: dns\dns_soa_data.htm
tech.root: DNS
ms.assetid: 715cbb70-91fe-47ac-a713-1fe0701d4f8c
ms.date: 01/15/2025
ms.keywords: '*PDNS_SOA_DATA, *PDNS_SOA_DATAW, DNS_SOA_DATA, DNS_SOA_DATA structure [DNS], DNS_SOA_DATAW, PDNS_SOA_DATA, PDNS_SOA_DATA structure pointer [DNS], _dns_dns_soa_data, dns.dns_soa_data, windnsdef/DNS_SOA_DATA, windnsdef/PDNS_SOA_DATA'
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
req.typenames: DNS_SOA_DATAW, *PDNS_SOA_DATAW
req.redist: 

f1_keywords:
 - PDNS_SOA_DATAW
 - windnsdef/PDNS_SOA_DATAW
 - DNS_SOA_DATAW
 - windnsdef/DNS_SOA_DATAW
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
 - DNS_SOA_DATA
---

# DNS_SOA_DATAW structure


## -description

The 
<b>DNS_SOA_DATA</b> structure represents a DNS start of authority (SOA) record as specified in section 3.3.13 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.

## -struct-fields

### -field pNamePrimaryServer

A pointer to a string that represents the name of the authoritative DNS server for the zone to which the record belongs.

### -field pNameAdministrator

A pointer to a string that represents the name of the responsible party for the zone to which the record belongs.

### -field dwSerialNo

The serial number of the SOA record.

### -field dwRefresh

The time, in seconds, before the zone containing this record should be refreshed.

### -field dwRetry

The time, in seconds, before retrying a failed refresh of the zone to which this record belongs.

### -field dwExpire

The time, in seconds, before an unresponsive zone is no longer authoritative.

### -field dwDefaultTtl

The lower limit on the time, in seconds, that a DNS server or caching resolver are allowed to cache any resource records (RR) from the zone to which this record belongs.

## -remarks

The 
<b>DNS_SOA_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.





> [!NOTE]
> The windns.h header defines DNS_SOA_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

