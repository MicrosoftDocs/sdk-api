---
UID: NF:windns.DnsRecordListFree
title: DnsRecordListFree macro
author: windows-sdk-content
description: Frees memory allocated for DNS records obtained using the DnsQuery function.
old-location: dns\dnsrecordlistfree.htm
old-project: DNS
ms.assetid: fc4c0cb4-646f-4946-8f07-b5a858f7064a
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: DnsRecordListFree, DnsRecordListFree function [DNS], _dns_dnsrecordlistfree, dns.dnsrecordlistfree, windns/DnsRecordListFree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dnsapi.dll
api_name:
-	DnsRecordListFree
product: Windows
targetos: Windows
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DnsRecordListFree macro


## -description



			The 
<b>DnsRecordListFree</b> function frees memory allocated for DNS records obtained using the 
<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a> function.


## -parameters




### -param p

TBD


### -param t

TBD






#### - FreeType [in]

A specifier of how the record list should be freed. The only type currently supported is a deep freeing of the entire record list. For more information and a list of values, see the <a href="https://msdn.microsoft.com/976982a1-08f1-4c67-b823-1eea34f0c643">DNS_FREE_TYPE</a> enumeration.


#### - pRecordList [in, out, optional]

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the list of DNS records to be freed.


## -remarks



The 
<b>DnsRecordListFree</b> function can be used to free memory allocated from query results obtained using a 
<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a> function call; it cannot free memory allocated for DNS record lists created manually.




## -see-also




<a href="https://msdn.microsoft.com/976982a1-08f1-4c67-b823-1eea34f0c643">DNS_FREE_TYPE</a>
 

 

