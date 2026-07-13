---
UID: NS:windnsdef._DnsAddrArray
title: DNS_ADDR_ARRAY (windnsdef.h)
description: Stores an array of IPv4 or IPv6 addresses.
helpviewer_keywords: ["*PDNS_ADDR_ARRAY","AF_INET","AF_INET6","DNS_ADDR_ARRAY","DNS_ADDR_ARRAY structure [DNS]","PDNS_ADDR_ARRAY","PDNS_ADDR_ARRAY structure pointer [DNS]","dns.dns_addr_array","windnsdef/DNS_ADDR_ARRAY","windnsdef/PDNS_ADDR_ARRAY"]
old-location: dns\dns_addr_array.htm
tech.root: DNS
ms.assetid: 5FD7F28B-D1A6-4731-ACB9-A7BB23CC1FB4
ms.date: 01/15/2025
ms.keywords: '*PDNS_ADDR_ARRAY, AF_INET, AF_INET6, DNS_ADDR_ARRAY, DNS_ADDR_ARRAY structure [DNS], PDNS_ADDR_ARRAY, PDNS_ADDR_ARRAY structure pointer [DNS], dns.dns_addr_array, windnsdef/DNS_ADDR_ARRAY, windnsdef/PDNS_ADDR_ARRAY'
req.header: windnsdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DNS_ADDR_ARRAY, *PDNS_ADDR_ARRAY
req.redist: 

f1_keywords:
 - _DnsAddrArray
 - windnsdef/_DnsAddrArray
 - PDNS_ADDR_ARRAY
 - windnsdef/PDNS_ADDR_ARRAY
 - DNS_ADDR_ARRAY
 - windnsdef/DNS_ADDR_ARRAY
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
 - DNS_ADDR_ARRAY
---

# DNS_ADDR_ARRAY structure


## -description

The <b>DNS_ADDR_ARRAY</b> structure stores an array of IPv4 or IPv6 addresses.

## -struct-fields

### -field MaxCount

Indicates, the size, in bytes,  of this structure.

### -field AddrCount

Indicates the number of <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_addr">DNS_ADDR</a> structures contained in the <b>AddrArray</b> member.

### -field Tag

Reserved. Do not use.

### -field Family

A value that specifies the IP family. Possible values are:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
</dl>
</td>
<td width="60%">
IPv6

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
</dl>
</td>
<td width="60%">
IPv4

</td>
</tr>
</table>

### -field WordReserved

Reserved. Do not use.

### -field Flags

Reserved. Do not use.

### -field MatchFlag

Reserved. Do not use.

### -field Reserved1

Reserved. Do not use.

### -field Reserved2

Reserved. Do not use.

### -field AddrArray

An array of <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_addr">DNS_ADDR</a> structures that each contain an IP address.

### -field AddrArray.size_is

### -field AddrArray.size_is.AddrCount

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_addr">DNS_ADDR</a>



<a href="/windows/win32/api/windnsdef/ns-windns-dns_query_result">DNS_QUERY_RESULT</a>