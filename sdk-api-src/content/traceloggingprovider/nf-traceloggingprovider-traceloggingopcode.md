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

# TraceLoggingOpcode macro


## -description


Wrapper macro for setting the event's opcode. 


## -parameters




### -param eventOpcode [in]

The event opcode. The event opcode must be a compile-time constant between 0 and 255. 


## -remarks



If TraceLoggingOpcode has no provided argument, the  default opcode is 0 (EVENT_TRACE_TYPE_INFO). If multiple arguments are provided, the value from the previous call to  TraceLoggingOpcode is used.



