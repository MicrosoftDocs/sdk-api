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

# IPV6_LOCAL_BINDING structure


## -description


The 
<b>IPV6_LOCAL_BINDING</b> structure contains IPv6 address information for an adapter.


## -struct-fields




### -field Address

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">in6_addr</a> structure that specifies an IPv6 address for the adapter.


### -field PrefixLength

The length, in bits, of the address prefix.


## -remarks



Since an adapter can have more than one IP address, the 
<a href="https://msdn.microsoft.com/1e964f09-96c6-432b-bb1a-026a3ea0deba">IPV6_ADAPTER_BINDING_INFO</a> structure maintains an array of 
<b>IPV6_LOCAL_BINDING</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/1e964f09-96c6-432b-bb1a-026a3ea0deba">IPV6_ADAPTER_BINDING_INFO</a>



<a href="https://msdn.microsoft.com/121cc415-35eb-4c9b-a02d-c23be468d6bc">IP_LOCAL_BINDING</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

