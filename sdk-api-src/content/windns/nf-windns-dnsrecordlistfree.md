---
UID: NF:windns.DnsRecordListFree
title: DnsRecordListFree macro (windns.h)

description: Frees memory allocated for DNS records obtained using the DnsQuery function.
old-location: dns\dnsrecordlistfree.htm
tech.root: DNS
ms.assetid: fc4c0cb4-646f-4946-8f07-b5a858f7064a

ms.date: 12/05/2018
ms.keywords: DnsRecordListFree, DnsRecordListFree function [DNS], _dns_dnsrecordlistfree, dns.dnsrecordlistfree, windns/DnsRecordListFree
ms.topic: macro
f1_keywords: 
 - "windns/DnsRecordListFree"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsRecordListFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DnsRecordListFree macro


## -description


The 
<b>DnsRecordListFree</b> function frees memory allocated for DNS records obtained using the 
<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a> function.


## -parameters




### -param p [in, out, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure that contains the list of DNS records to be freed.


### -param t [in]

A specifier of how the record list should be freed. The only type currently supported is a deep freeing of the entire record list. For more information and a list of values, see the <a href="https://docs.microsoft.com/windows/win32/api/windns/ne-windns-dns_free_type">DNS_FREE_TYPE</a> enumeration.


## -remarks



The 
<b>DnsRecordListFree</b> function can be used to free memory allocated from query results obtained using a 
<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a> function call; it cannot free memory allocated for DNS record lists created manually.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/windns/ne-windns-dns_free_type">DNS_FREE_TYPE</a>
 

 

