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

# _WSMAN_SHELL_ASYNC structure


## -description


Defines an asynchronous structure to be passed to all shell operations. It contains an optional user context and the callback function.


## -struct-fields




### -field operationContext

Specifies the optional user context associated with the operation.


### -field completionFunction

Specifies the <a href="https://msdn.microsoft.com/705732a8-7584-42cf-be9b-dd36b35bba37">WSMAN_SHELL_COMPLETION_FUNCTION</a> callback function for the operation.

