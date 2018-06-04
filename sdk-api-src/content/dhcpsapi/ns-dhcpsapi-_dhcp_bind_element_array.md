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

# _DHCP_BIND_ELEMENT_ARRAY structure


## -description


The <b>DHCP_BIND_ELEMENT_ARRAY</b> structure defines an array of network binding elements used by a DHCP server.


## -struct-fields




### -field NumElements

Specifies the number of network binding elements listed in <i>Elements</i>.


### -field Elements

Specifies an array of <a href="https://msdn.microsoft.com/00d9d23e-fb39-4f3c-a2b9-9983322879fd">DHCP_BIND_ELEMENT</a> structures


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/00d9d23e-fb39-4f3c-a2b9-9983322879fd">DHCP_BIND_ELEMENT</a>



<a href="https://msdn.microsoft.com/c0f5c9c1-d421-4977-aa26-1b8b7406802d">DhcpGetServerBindingInfo</a>



<a href="https://msdn.microsoft.com/6291e266-e9d5-4899-8b34-53695f49a1b8">DhcpSetServerBindingInfo</a>
 

 

