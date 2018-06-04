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

# _IP_UNIDIRECTIONAL_ADAPTER_ADDRESS structure


## -description



			The 
<b>IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</b> structure stores the IPv4 addresses associated with a unidirectional adapter.


## -struct-fields




### -field NumAdapters

The number of IPv4 addresses pointed to by the <b>Address</b> member.


### -field Address

An array of variables of type <a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a>. Each element of the array specifies an IPv4 address associated with this unidirectional adapter.


## -remarks



The <b>IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</b> structure is retrieved by the <a href="https://msdn.microsoft.com/32aa3a8e-ae74-4da9-bc8d-b28e270d9702">GetUnidirectionalAdapterInfo</a>
		 function. A unidirectional adapter is an adapter that can receive
    IPv4 datagrams, but can't transmit them.





## -see-also




<a href="https://msdn.microsoft.com/32aa3a8e-ae74-4da9-bc8d-b28e270d9702">GetUnidirectionalAdapterInfo</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a>
 

 

