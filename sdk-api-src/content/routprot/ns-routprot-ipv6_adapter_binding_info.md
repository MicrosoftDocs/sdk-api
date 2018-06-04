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

# IPV6_ADAPTER_BINDING_INFO structure


## -description


The 
<b>IPV6_ADAPTER_BINDING_INFO</b> structure contains IPv6-specific information for a particular network adapter.


## -struct-fields




### -field AddressCount

The number of IPv6 addresses associated with this adapter.


### -field RemoteAddress

This member is for WAN interfaces. An <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">in6_addr</a> structure that contains the address of the machine at the other end of a dial-up link.


### -field Mtu

Reserved for future use.


### -field Speed

Reserved for future use.


### -field Address

Pointer to an array of 
<a href="https://msdn.microsoft.com/c698fa3b-04d5-4401-9ab3-a200211cff24">IPV6_LOCAL_BINDING</a> structures. The array  contains a structure for each of the IPv6 addresses associated with this adapter.


## -remarks



Since an adapter can have more than one IP address, the 
<b>IPV6_ADAPTER_BINDING_INFO</b> structure maintains an array of 
<a href="https://msdn.microsoft.com/c698fa3b-04d5-4401-9ab3-a200211cff24">IPV6_LOCAL_BINDING</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/c698fa3b-04d5-4401-9ab3-a200211cff24">IPV6_LOCAL_BINDING</a>



<a href="https://msdn.microsoft.com/3eb864e7-2de6-44c2-af3e-fee547de6081">IP_ADAPTER_BINDING_INFO</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

