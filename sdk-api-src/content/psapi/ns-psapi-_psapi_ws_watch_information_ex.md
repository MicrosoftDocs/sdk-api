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

# _PSAPI_WS_WATCH_INFORMATION_EX structure


## -description


Contains extended information about a page added to a process working set.


## -struct-fields




### -field BasicInfo

A <a href="https://msdn.microsoft.com/61083366-2a55-431c-807a-3eb85ba0b347">PSAPI_WS_WATCH_INFORMATION</a> structure.


### -field FaultingThreadId

The identifier of the thread that caused the page fault.


### -field Flags

This member is reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/8572db5c-2ffc-424f-8cec-b6a6902fed62">GetWsChangesEx</a>



<a href="https://msdn.microsoft.com/61083366-2a55-431c-807a-3eb85ba0b347">PSAPI_WS_WATCH_INFORMATION</a>
 

 

