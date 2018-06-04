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

# _PSAPI_WS_WATCH_INFORMATION structure


## -description


Contains information about a page added to a process working set.


## -struct-fields




### -field FaultingPc

A pointer to the instruction that caused the page fault.


### -field FaultingVa

A pointer to the page that was added to the working set.


## -see-also




<a href="https://msdn.microsoft.com/ace5106c-9c7b-4d5f-a69a-c3a8bff0bb2d">GetWsChanges</a>
 

 

