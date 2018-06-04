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

# IP_ADAPTER_BINDING_INFO structure


## -description


The 
<b>IP_ADAPTER_BINDING_INFO</b> structure contains IP-specific information for a particular network adapter.


## -struct-fields




### -field AddressCount

The number of IP addresses associated with this adapter.


### -field RemoteAddress

This member is for WAN interfaces. It contains the address of the machine at the other end of a dial-up link.


### -field Mtu

Reserved for future use.


### -field Speed

Reserved for future use.


### -field Address

Pointer to an array of 
<a href="https://msdn.microsoft.com/121cc415-35eb-4c9b-a02d-c23be468d6bc">IP_LOCAL_BINDING</a> structures. The array  contains a structure for each of the IP addresses associated with this adapter.


## -remarks



Since an adapter can have more than one IP address, the 
<b>IP_ADAPTER_BINDING_INFO</b> structure maintains an array of 
<a href="https://msdn.microsoft.com/121cc415-35eb-4c9b-a02d-c23be468d6bc">IP_LOCAL_BINDING</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/121cc415-35eb-4c9b-a02d-c23be468d6bc">IP_LOCAL_BINDING</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

