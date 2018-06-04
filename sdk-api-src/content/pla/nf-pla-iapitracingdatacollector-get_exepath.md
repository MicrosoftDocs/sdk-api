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

# IApiTracingDataCollector::get_ExePath


## -description


Retrieves or sets the path to the executable file whose API calls you want to trace.

This property is read/write.


## -parameters


## -remarks



If the executable file is currently running, the trace occurs the next time the executable file runs, not at this time.




## -see-also




<a href="https://msdn.microsoft.com/8d600d35-bd2b-44fc-9da4-3c6e50e90b65">IApiTracingDataCollector</a>



<a href="https://msdn.microsoft.com/ec97533c-88a7-4360-bc2d-8e6465256032">IApiTracingDataCollector::IncludeModules</a>
 

 

