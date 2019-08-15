---
UID: NF:windns.DnsRecordCompare
title: DnsRecordCompare function (windns.h)
author: windows-sdk-content
description: The DnsRecordCompare function compares two DNS resource records (RR).
old-location: dns\dnsrecordcompare.htm
tech.root: DNS
ms.assetid: c4449a23-d6d3-4f27-a963-a84144983e5e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DnsRecordCompare, DnsRecordCompare function [DNS], _dns_dnsrecordcompare, dns.dnsrecordcompare, windns/DnsRecordCompare
ms.topic: function
f1_keywords: 
 - "windns/DnsRecordCompare"
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
 - DnsRecordCompare
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DnsRecordCompare function


## -description


The 
<b>DnsRecordCompare</b> function compares two DNS resource records (RR).


## -parameters




### -param pRecord1 [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure that contains the first DNS RR of the comparison pair.


### -param pRecord2 [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure that contains the second DNS RR of the comparison pair.


## -returns



Returns <b>TRUE</b> if the compared records are equivalent, <b>FALSE</b> if they are not.




## -remarks



When comparing records, DNS RRs that are stored using different character encoding are treated by the 
<b>DnsRecordCompare</b> function as different, even if the records are otherwise equivalent.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsrecordsetcompare">DnsRecordSetCompare</a>
 

 

