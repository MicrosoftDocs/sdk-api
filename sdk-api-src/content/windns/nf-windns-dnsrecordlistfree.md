---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

