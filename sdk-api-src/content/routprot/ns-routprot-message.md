---
UID: NS:routprot._MESSAGE
title: MESSAGE (routprot.h)
author: windows-sdk-content
description: The MESSAGE union contains information about an event reported to the router manager through the routing protocol's message queue.
old-location: rras\message.htm
tech.root: RRAS
ms.assetid: 94f3069f-c282-4dea-84f9-48645f4e1593
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMESSAGE, MESSAGE, MESSAGE structure [RAS], PMESSAGE, PMESSAGE structure pointer [RAS], _MESSAGE, _mpr_message, routprot/MESSAGE, routprot/PMESSAGE, rras.message"
ms.topic: struct
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Routprot.h
api_name:
 - MESSAGE
product: Windows
targetos: Windows
req.typenames: MESSAGE, *PMESSAGE
req.redist: 
---

# MESSAGE structure


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
 

 

