---
UID: NF:windns.DnsRecordSetDetach
title: DnsRecordSetDetach function
author: windows-sdk-content
description: The DnsRecordSetDetach function detaches the first record set from a specified list of DNS records.
old-location: dns\dnsrecordsetdetach.htm
old-project: DNS
ms.assetid: 434dc11f-19a9-434f-a024-9cdbb560f24c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DnsRecordSetDetach, DnsRecordSetDetach function [DNS], _dns_dnsrecordsetdetach, dns.dnsrecordsetdetach, windns/DnsRecordSetDetach
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DNS_FREE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsRecordSetDetach
product: Windows
targetos: Windows
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DnsRecordSetDetach function


## -description


The <b>DnsRecordSetDetach</b> function detaches the first record set from a specified list of DNS records.


## -parameters




### -param pRecordList

TBD




#### - pRR [in, out]

A pointer, on input, to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the list prior to the detachment of the first DNS record in the list of DNS records.  A pointer, on output to a <b>DNS_RECORD</b> structure that contains the list subsequent to the detachment of the DNS record.


## -returns



On return, the <b>DnsRecordSetDetach</b> function points to the detached DNS record set.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>



<a href="https://msdn.microsoft.com/c4449a23-d6d3-4f27-a963-a84144983e5e">DnsRecordCompare</a>



<a href="https://msdn.microsoft.com/008cf2ba-ccb2-430a-85d9-68d424b6938f">DnsRecordSetCompare</a>
 

 

