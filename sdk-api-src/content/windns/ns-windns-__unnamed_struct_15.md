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

# DNS_AAAA_DATA structure


## -description


The 
<b>DNS_AAAA_DATA</b> structure represents a DNS IPv6 (AAAA) record as specified in <a href="http://go.microsoft.com/fwlink/p/?linkid=107027">RFC 3596</a>.


## -struct-fields




### -field Ip6Address

An <a href="https://msdn.microsoft.com/789400be-03c7-4c4f-9e78-fa2573cf114d">IP6_ADDRESS</a> data type that contains an IPv6 address.


## -remarks



The 
<b>DNS_AAAA_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

