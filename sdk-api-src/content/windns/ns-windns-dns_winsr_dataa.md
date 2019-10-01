---
UID: NS:windns.__unnamed_struct_42
title: DNS_WINSR_DATAA (windns.h)
author: windows-sdk-content
description: The DNS_WINSR_DATA structure represents a DNS Windows Internet Name Service reverse-lookup (WINSR) record.
old-location: dns\dns_winsr_data.htm
tech.root: DNS
ms.assetid: a7e79e30-905f-42a5-a4de-02d71adfe95e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDNS_WINSR_DATA, *PDNS_WINSR_DATAA, DNS_WINSR_DATA, DNS_WINSR_DATA structure [DNS], DNS_WINSR_DATAA, DNS_WINS_FLAG_LOCAL, DNS_WINS_FLAG_SCOPE, PDNS_WINSR_DATA, PDNS_WINSR_DATA structure pointer [DNS], _dns_dns_winsr_data, dns.dns_winsr_data, windns/DNS_WINSR_DATA, windns/PDNS_WINSR_DATA"
ms.topic: struct
f1_keywords: 
 - "windns/DNS_WINSR_DATA"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_WINSR_DATA
targetos: Windows
req.typenames: DNS_WINSR_DATAA, *PDNS_WINSR_DATAA
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>
 

 

