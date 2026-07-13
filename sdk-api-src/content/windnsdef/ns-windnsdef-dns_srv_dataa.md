---
UID: NS:windnsdef.DNS_SRV_DATAA
title: DNS_SRV_DATAA (windnsdef.h)
description: The DNS_SRV_DATA structure represents a DNS service (SRV) record as specified in RFC 2782. (ANSI)
helpviewer_keywords: ["*PDNS_SRV_DATA","*PDNS_SRV_DATAA","DNS_SRV_DATA","DNS_SRV_DATA structure [DNS]","DNS_SRV_DATAA","PDNS_SRV_DATA","PDNS_SRV_DATA structure pointer [DNS]","_dns_dns_srv_data","dns.dns_srv_data","windnsdef/DNS_SRV_DATA","windnsdef/PDNS_SRV_DATA"]
old-location: dns\dns_srv_data.htm
tech.root: DNS
ms.assetid: 212db7ac-a5e3-4e58-b1c2-0eb551403dfc
ms.date: 01/15/2025
ms.keywords: '*PDNS_SRV_DATA, *PDNS_SRV_DATAA, DNS_SRV_DATA, DNS_SRV_DATA structure [DNS], DNS_SRV_DATAA, PDNS_SRV_DATA, PDNS_SRV_DATA structure pointer [DNS], _dns_dns_srv_data, dns.dns_srv_data, windnsdef/DNS_SRV_DATA, windnsdef/PDNS_SRV_DATA'
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
req.typenames: DNS_SRV_DATAA, *PDNS_SRV_DATAA
req.redist: 

f1_keywords:
 - PDNS_SRV_DATAA
 - windnsdef/PDNS_SRV_DATAA
 - DNS_SRV_DATAA
 - windnsdef/DNS_SRV_DATAA
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
 - DNS_SRV_DATA
---

# DNS_SRV_DATAA structure


## -description

The 
<b>DNS_SRV_DATA</b> structure represents a DNS service (SRV) record as specified in <a href="https://www.ietf.org/rfc/rfc2782.txt">RFC 2782</a>.

## -struct-fields

### -field pNameTarget

A pointer to a string that represents the target host.

### -field wPriority

The priority of the target host specified in <b>pNameTarget</b>. Lower numbers imply higher priority to clients attempting to use this service.

### -field wWeight

The relative weight of the target host in <b>pNameTarget</b> to other hosts with the same <b>wPriority</b>. The chances of using this host should be proportional to its weight.

### -field wPort

The port used on the target host for this service.

### -field Pad

Reserved for padding. Do not use.

## -remarks

The 
<b>DNS_SRV_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.





> [!NOTE]
> The windns.h header defines DNS_SRV_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

