---
UID: NF:windns.DnsRecordCompare
title: DnsRecordCompare function
author: windows-sdk-content
description: The DnsRecordCompare function compares two DNS resource records (RR).
old-location: dns\dnsrecordcompare.htm
tech.root: dns
ms.assetid: c4449a23-d6d3-4f27-a963-a84144983e5e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DnsRecordCompare, DnsRecordCompare function [DNS], _dns_dnsrecordcompare, dns.dnsrecordcompare, windns/DnsRecordCompare
ms.topic: function
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
---

# DnsRecordCompare function


## -description


The 
<b>DnsRecordCompare</b> function compares two DNS resource records (RR).


## -parameters




### -param pRecord1 [in]

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the first DNS RR of the comparison pair.


### -param pRecord2 [in]

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the second DNS RR of the comparison pair.


## -returns



Returns <b>TRUE</b> if the compared records are equivalent, <b>FALSE</b> if they are not.




## -remarks



When comparing records, DNS RRs that are stored using different character encoding are treated by the 
<b>DnsRecordCompare</b> function as different, even if the records are otherwise equivalent.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/008cf2ba-ccb2-430a-85d9-68d424b6938f">DnsRecordSetCompare</a>
 

 

