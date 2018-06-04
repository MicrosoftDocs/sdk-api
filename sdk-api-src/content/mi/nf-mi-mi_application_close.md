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

# MI_Application_Close function


## -description


Deinitializes the management infrastructure client API that was initialized through a call to <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a>.


## -parameters




### -param application [in, out]

Application handle that was initialized through a call to <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a>.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



<b>MI_Application_Close</b> will unload the entire protocol handling infrastructure and background threads associated with the infrastructure.

<b>MI_Application_Close</b> cancels all active sessions and operations.  Sessions created under the target application and those sessions' operations must close before this function will return. Once the API does so, Mi.dll can be unloaded and any caches held within the MI infrastructure are flushed.

<b>MI_Application_Close</b> must not be called from within an asynchronous callback, otherwise it will cause deadlocks.

To avoid a system hang when calling this function, reference count <a href="https://msdn.microsoft.com/da486ade-88ef-40c4-8151-356e718da7db">MI_Application</a> and call the <b>MI_Application_Close</b> function only when the AppDomain is shutting down and after all sessions have been closed.



