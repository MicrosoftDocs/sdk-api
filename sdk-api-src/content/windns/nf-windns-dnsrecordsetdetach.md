---
UID: NF:windns.DnsRecordSetDetach
title: DnsRecordSetDetach function (windns.h)
description: The DnsRecordSetDetach function detaches the first record set from a specified list of DNS records.
helpviewer_keywords: ["DnsRecordSetDetach","DnsRecordSetDetach function [DNS]","_dns_dnsrecordsetdetach","dns.dnsrecordsetdetach","windns/DnsRecordSetDetach"]
old-location: dns\dnsrecordsetdetach.htm
tech.root: DNS
ms.assetid: 434dc11f-19a9-434f-a024-9cdbb560f24c
ms.date: 12/05/2018
ms.keywords: DnsRecordSetDetach, DnsRecordSetDetach function [DNS], _dns_dnsrecordsetdetach, dns.dnsrecordsetdetach, windns/DnsRecordSetDetach
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
 - DnsRecordSetDetach
 - windns/DnsRecordSetDetach
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
 - DnsRecordSetDetach
---

# DnsRecordSetDetach function


## -description

The <b>DnsRecordSetDetach</b> function detaches the first record set from a specified list of DNS records.

## -parameters

### -param pRecordList [in, out]

A pointer, on input, to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the list prior to the detachment of the first DNS record in the list of DNS records.  A pointer, on output to a <b>DNS_RECORD</b> structure that contains the list subsequent to the detachment of the DNS record.

## -returns

On return, the <b>DnsRecordSetDetach</b> function points to the detached DNS record set.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsrecordcompare">DnsRecordCompare</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsrecordsetcompare">DnsRecordSetCompare</a>