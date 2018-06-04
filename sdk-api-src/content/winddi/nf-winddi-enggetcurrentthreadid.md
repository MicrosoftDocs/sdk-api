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

# EngGetCurrentThreadId function


## -description


The <b>EngGetCurrentThreadId</b> function identifies an application's current thread.


## -parameters






## -returns



<b>EngGetCurrentThreadId</b> returns the 4-byte identifier of the application's thread.




## -remarks



Callers of <b>EngGetCurrentThreadId</b> should treat the returned ID as a read-only value. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564919">EngGetCurrentProcessId</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564955">EngGetProcessHandle</a>
 

 

