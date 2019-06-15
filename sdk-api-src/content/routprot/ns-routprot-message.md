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
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/routprot/nc-routprot-pdo_update_routes">DoUpdateRoutes</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa374005(v=vs.85)">DoUpdateServices</a>



<a href="https://docs.microsoft.com/windows/desktop/api/routprot/nc-routprot-pget_event_message">GetEventMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/routing-protocol-interface-structures">Routing Protocol Interface Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/routprot/ns-routprot-_update_complete_message">UPDATE_COMPLETE_MESSAGE</a>
 

 

