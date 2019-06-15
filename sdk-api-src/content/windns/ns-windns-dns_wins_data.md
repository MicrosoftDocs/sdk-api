---
UID: NS:windns.__unnamed_struct_40
title: DNS_WINS_DATA (windns.h)
author: windows-sdk-content
description: The DNS_WINS_DATA structure represents a DNS Windows Internet Name Service (WINS) record.
old-location: dns\dns_wins_data.htm
tech.root: DNS
ms.assetid: df41c397-e662-42b4-9193-6776f9071898
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDNS_WINS_DATA, DNS_WINS_DATA, DNS_WINS_DATA structure [DNS], DNS_WINS_FLAG_LOCAL, DNS_WINS_FLAG_SCOPE, PDNS_WINS_DATA, PDNS_WINS_DATA structure pointer [DNS], _dns_dns_wins_data, dns.dns_wins_data, windns/DNS_WINS_DATA, windns/PDNS_WINS_DATA"
ms.topic: struct
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
 - DNS_WINS_DATA
product: Windows
targetos: Windows
req.typenames: DNS_WINS_DATA, *PDNS_WINS_DATA
req.redist: 
ms.custom: 19H1
---

# DNS_WINS_DATA structure


## -description


The 
<b>DNS_WINS_DATA</b> structure represents a DNS Windows Internet Name Service (WINS) record.


## -struct-fields




### -field dwMappingFlag

The WINS mapping flag that specifies whether the record must be included in zone replication. <b>dwMappingFlag</b> must be one of these mutually exclusive values:

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


### -field cWinsServerCount

The number of WINS Servers listed in <b>WinsServers</b>.


### -field WinsServers

An array of <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-_ip4_array">IP4_ARRAY</a> structures that contain the IPv4 address of the WINS lookup Servers.


## -remarks



The 
<b>DNS_WINS_DATA</b> structure is used in conjunction with the 
<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-_dnsrecorda">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-_dnsrecorda">DNS_RECORD</a>
 

 

