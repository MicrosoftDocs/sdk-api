---
UID: NF:windns.DnsRecordSetCompare
title: DnsRecordSetCompare function (windns.h)
description: The DnsRecordSetCompare function compares two RR sets.
helpviewer_keywords: ["DnsRecordSetCompare","DnsRecordSetCompare function [DNS]","_dns_dnsrecordsetcompare","dns.dnsrecordsetcompare","windns/DnsRecordSetCompare"]
old-location: dns\dnsrecordsetcompare.htm
tech.root: DNS
ms.assetid: 008cf2ba-ccb2-430a-85d9-68d424b6938f
ms.date: 12/05/2018
ms.keywords: DnsRecordSetCompare, DnsRecordSetCompare function [DNS], _dns_dnsrecordsetcompare, dns.dnsrecordsetcompare, windns/DnsRecordSetCompare
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
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsRecordSetCompare
 - windns/DnsRecordSetCompare
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
 - DnsRecordSetCompare
---

# DnsRecordSetCompare function


## -description

The 
<b>DnsRecordSetCompare</b> function compares two RR sets.

## -parameters

### -param pRR1 [in, out]

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the first DNS RR set of the comparison pair.

### -param pRR2 [in, out]

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the second DNS resource record set of the comparison pair.

### -param ppDiff1 [out, optional]

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> pointer that contains the list of resource records built as a result of the arithmetic performed on them: <b>pRRSet1</b> minus <b>pRRSet2</b>.

### -param ppDiff2 [out, optional]

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> pointer that contains the list of resource records built as a result of the arithmetic performed on them: <b>pRRSet2</b> minus <b>pRRSet1</b>.

## -returns

Returns <b>TRUE</b> if the compared record sets are equivalent, <b>FALSE</b> if they are not.

## -remarks

When comparing record sets, DNS resource records that are stored using different character encoding are treated by the 
<b>DnsRecordSetCompare</b> function as equivalent. Contrast this to the 
<a href="/windows/desktop/api/windns/nf-windns-dnsrecordcompare">DnsRecordCompare</a> function, in which equivalent records with different encoding are not returned as equivalent records.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsrecordcompare">DnsRecordCompare</a>