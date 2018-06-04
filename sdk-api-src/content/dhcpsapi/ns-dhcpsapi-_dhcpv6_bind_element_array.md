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

# _DHCPV6_BIND_ELEMENT_ARRAY structure


## -description


The <b>DHCPV6_BIND_ELEMENT_ARRAY</b> structure specifies an array of <a href="https://msdn.microsoft.com/7c5b1d5d-7c91-46a8-aaa0-1d957430461d">DHCPV6_BIND_ELEMENT</a> structures that contain DHCPv6 interface bindings.


## -struct-fields




### -field NumElements

Integer that contains the total number of elements in the array pointed to by <b>Elements</b>.


### -field Elements

Pointer to an array of <a href="https://msdn.microsoft.com/7c5b1d5d-7c91-46a8-aaa0-1d957430461d">DHCPV6_BIND_ELEMENT</a> structures that contains the DHCPv6 interface bindings.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/7c5b1d5d-7c91-46a8-aaa0-1d957430461d">DHCPV6_BIND_ELEMENT</a>
 

 

