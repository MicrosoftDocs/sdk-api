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

# IP_LOCAL_BINDING structure


## -description


The 
<b>IP_LOCAL_BINDING</b> structure contains IP address information for an adapter.


## -struct-fields




### -field Address

Specifies an IP address for the adapter.


### -field Mask

Specifies the subnet mask for the IP address.


## -remarks



Since an adapter can have more than one IP address, the 
<a href="https://msdn.microsoft.com/3eb864e7-2de6-44c2-af3e-fee547de6081">IP_ADAPTER_BINDING_INFO</a> structure maintains an array of 
<b>IP_LOCAL_BINDING</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/3eb864e7-2de6-44c2-af3e-fee547de6081">IP_ADAPTER_BINDING_INFO</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

