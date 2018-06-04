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

# _RTM_ENTITY_INFO structure


## -description


The 
<b>RTM_ENTITY_INFO</b> structure is used to exchange client information with the routing table manager.


## -struct-fields




### -field RtmInstanceId

Specifies the instance of the routing table manager with which the client registered.


### -field AddressFamily

Specifies the address family to which the client belongs.


### -field EntityId

Specifies the identifier that uniquely identifies a client.


## -see-also




<a href="https://msdn.microsoft.com/6c75fb17-60b9-44cb-a934-430a6de74ee7">RTM_ENTITY_ID</a>



<a href="https://msdn.microsoft.com/6062369c-22c7-48e4-9dd3-91efba22df34">RtmGetEntityInfo</a>



<a href="https://msdn.microsoft.com/411e15bc-7f47-4ef7-9400-292203b581af">RtmGetRegisteredEntities</a>



<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>



<a href="https://msdn.microsoft.com/ea72dde4-2d04-4ceb-b718-3ee96bf70464">RtmReleaseEntityInfo</a>
 

 

