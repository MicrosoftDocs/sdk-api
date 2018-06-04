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

# _MESSAGE structure


## -description


The 
<b>MESSAGE</b> union contains information about an event reported to the router manager through the routing protocol's message queue.


## -struct-fields




### -field UpdateCompleteMessage

Provides information associated with an UPDATE_COMPLETE event.


### -field InterfaceIndex

Identifies the interface associated with a SAVE_INTERFACE_CONFIG_INFO event.


## -see-also




<a href="https://msdn.microsoft.com/5942c856-f504-4e2d-86c8-f3207c787ed5">DoUpdateRoutes</a>



<a href="https://msdn.microsoft.com/1e7b5e3c-0d90-445e-93a3-57ee08d19ec2">DoUpdateServices</a>



<a href="https://msdn.microsoft.com/59aa7bd8-3510-4ca0-90f1-2667dcb4abf0">GetEventMessage</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>



<a href="https://msdn.microsoft.com/679c74fa-0049-4556-a942-e51160ceb796">Routing Protocol Interface Structures</a>



<a href="https://msdn.microsoft.com/76f00da0-4f56-4a1a-977d-a3872bbe19fc">UPDATE_COMPLETE_MESSAGE</a>
 

 

