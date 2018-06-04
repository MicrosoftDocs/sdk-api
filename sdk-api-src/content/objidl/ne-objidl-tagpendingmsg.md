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

# tagPENDINGMSG enumeration


## -description


Specifies the return values for the <a href="https://msdn.microsoft.com/f4aff53f-c344-4456-b53e-296d5a5b653a">IMessageFilter::MessagePending</a> method.


## -enum-fields




### -field PENDINGMSG_CANCELCALL

Cancel the outgoing call.


### -field PENDINGMSG_WAITNOPROCESS

Wait for the return and don't dispatch the message.


### -field PENDINGMSG_WAITDEFPROCESS

Wait and dispatch the message.


## -see-also




<a href="https://msdn.microsoft.com/f4aff53f-c344-4456-b53e-296d5a5b653a">IMessageFilter::MessagePending</a>
 

 

