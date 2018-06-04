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

# IsProcessCritical function


## -description


Determines whether the specified process is considered critical.


## -parameters




### -param hProcess [in]

A handle to the process to query. The process must have been          opened with <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access.  


### -param Critical [out]

A pointer to the <b>BOOL</b> value this function will use to indicate whether the process          is considered critical.  


## -returns



This routine returns FALSE on failure. Any other value indicates success.      Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to query for the specific error reason on failure.




## -see-also




<a href="https://msdn.microsoft.com/40e6f80d-a778-4d5f-bb1b-db294815f8b5">HRESULT_FROM_WIN32</a>
 

 

