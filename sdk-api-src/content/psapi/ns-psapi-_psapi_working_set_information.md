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

# _PSAPI_WORKING_SET_INFORMATION structure


## -description


Contains working set information for a process.


## -struct-fields




### -field NumberOfEntries

The number of entries in the <b>WorkingSetInfo</b> array.


### -field WorkingSetInfo

An array of <a href="https://msdn.microsoft.com/feb64235-1003-4595-a6a9-aca1f94f94b8">PSAPI_WORKING_SET_BLOCK</a> elements, one for each page in the process working set.


## -see-also




<a href="https://msdn.microsoft.com/feb64235-1003-4595-a6a9-aca1f94f94b8">PSAPI_WORKING_SET_BLOCK</a>



<a href="https://msdn.microsoft.com/b932153f-2bbd-460e-8ff7-b3e493c397bb">QueryWorkingSet</a>
 

 

