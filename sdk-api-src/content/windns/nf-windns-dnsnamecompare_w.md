---
UID: NF:windns.DnsNameCompare_W
title: DnsNameCompare_W function (windns.h)
description: The DnsNameCompare function compares two DNS names. (DnsNameCompare_W)
helpviewer_keywords: ["DnsNameCompare", "DnsNameCompare function [DNS]", "DnsNameCompare_UTF8", "DnsNameCompare_W", "_dns_dnsnamecompare", "dns.dnsnamecompare", "windns/DnsNameCompare", "windns/DnsNameCompare_UTF8", "windns/DnsNameCompare_W"]
old-location: dns\dnsnamecompare.htm
tech.root: DNS
ms.assetid: 4a1512b3-8273-4632-9426-daa36456bce3
ms.date: 12/05/2018
ms.keywords: DnsNameCompare, DnsNameCompare function [DNS], DnsNameCompare_A, DnsNameCompare_UTF8, DnsNameCompare_W, _dns_dnsnamecompare, dns.dnsnamecompare, windns/DnsNameCompare, windns/DnsNameCompare_A, windns/DnsNameCompare_UTF8, windns/DnsNameCompare_W
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DnsNameCompare_W (Unicode) and DnsNameCompare_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsNameCompare_W
 - windns/DnsNameCompare_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsNameCompare
 - DnsNameCompare_A
 - DnsNameCompare_W
 - DnsNameCompare_UTF8
---

# DnsNameCompare_W function


## -description

The 
<b>DnsNameCompare</b> function compares two DNS names. Like many DNS functions, the 
<b>DnsNameCompare</b> function type is implemented in multiple forms to facilitate different character encoding. Based on the character encoding involved, use one of the following functions:
<ul>
<li>
<b>DnsNameCompare_A</b> (_A for ANSI encoding)

</li>
<li>
<b>DnsNameCompare_W</b> (_W for Unicode encoding)

</li>
<li>
<b>DnsNameCompare_UTF8</b> (_UTF8 for Unicode encoding)

</li>
</ul>

## -parameters

### -param pName1 [in]

A pointer to a string that represents the first DNS name of the comparison pair.

### -param pName2 [in]

A pointer to a string that represents the second DNS name of the comparison pair.

## -returns

Returns <b>TRUE</b> if the compared names are equivalent, <b>FALSE</b> if they are not.

## -remarks

Name comparisons are not case sensitive, and trailing dots are ignored.

As with other DNS comparison functions, the 
<b>DnsNameCompare</b> function deems different encoding as an immediate indication of differing values, and as such, the same names with different characters encoding will not be reported identically.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsrecordcompare">DnsRecordCompare</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsrecordsetcompare">DnsRecordSetCompare</a>
