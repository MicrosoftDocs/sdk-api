---
UID: NS:windnsdef.DNS_WINSR_DATAA
title: DNS_WINSR_DATAA (windnsdef.h)
description: The DNS_WINSR_DATA structure represents a DNS Windows Internet Name Service reverse-lookup (WINSR) record. (ANSI)
helpviewer_keywords: ["*PDNS_WINSR_DATA","*PDNS_WINSR_DATAA","DNS_WINSR_DATA","DNS_WINSR_DATA structure [DNS]","DNS_WINSR_DATAA","DNS_WINS_FLAG_LOCAL","DNS_WINS_FLAG_SCOPE","PDNS_WINSR_DATA","PDNS_WINSR_DATA structure pointer [DNS]","_dns_dns_winsr_data","dns.dns_winsr_data","windnsdef/DNS_WINSR_DATA","windnsdef/PDNS_WINSR_DATA"]
old-location: dns\dns_winsr_data.htm
tech.root: DNS
ms.assetid: a7e79e30-905f-42a5-a4de-02d71adfe95e
ms.date: 01/15/2025
ms.keywords: '*PDNS_WINSR_DATA, *PDNS_WINSR_DATAA, DNS_WINSR_DATA, DNS_WINSR_DATA structure [DNS], DNS_WINSR_DATAA, DNS_WINS_FLAG_LOCAL, DNS_WINS_FLAG_SCOPE, PDNS_WINSR_DATA, PDNS_WINSR_DATA structure pointer [DNS], _dns_dns_winsr_data, dns.dns_winsr_data, windnsdef/DNS_WINSR_DATA, windnsdef/PDNS_WINSR_DATA'
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
req.typenames: DNS_WINSR_DATAA, *PDNS_WINSR_DATAA
req.redist: 

f1_keywords:
 - PDNS_WINSR_DATAA
 - windnsdef/PDNS_WINSR_DATAA
 - DNS_WINSR_DATAA
 - windnsdef/DNS_WINSR_DATAA
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
 - DNS_WINSR_DATA
---

# DNS_WINSR_DATAA structure


## -description

The 
<b>DNS_WINSR_DATA</b> structure represents a DNS Windows Internet Name Service reverse-lookup (WINSR) record.

## -struct-fields

### -field dwMappingFlag

The WINS mapping flag that specifies whether the record must be included into the zone replication. <b>dwMappingFlag</b> must be one of these mutually exclusive values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DNS_WINS_FLAG_SCOPE"></a><a id="dns_wins_flag_scope"></a><dl>
<dt><b>DNS_WINS_FLAG_SCOPE</b></dt>
</dl>
</td>
<td width="60%">
Record is not local, replicate across zones.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_WINS_FLAG_LOCAL"></a><a id="dns_wins_flag_local"></a><dl>
<dt><b>DNS_WINS_FLAG_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
Record is local, do not replicate.

</td>
</tr>
</table>

### -field dwLookupTimeout

The time, in seconds, that a DNS Server attempts resolution using WINS lookup.

### -field dwCacheTimeout

The time, in seconds, that a DNS Server using WINS lookup may cache the WINS Server's response.

### -field pNameResultDomain

A pointer to a string that represents the domain name to append to the name returned by a WINS reverse-lookup.

## -remarks

The 
<b>DNS_WINSR_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.





> [!NOTE]
> The windns.h header defines DNS_WINSR_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

