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

# EngIsSemaphoreOwned function


## -description


The <b>EngIsSemaphoreOwned</b> function determines whether any thread holds the specified semaphore.


## -parameters




### -param hsem [in]

Handle to the semaphore.


## -returns



<b>EngIsSemaphoreOwned</b> returns <b>TRUE</b> if any thread holds the specified semaphore, and <b>FALSE</b> if no thread holds it.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564760">EngCreateSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564961">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a>
 

 

