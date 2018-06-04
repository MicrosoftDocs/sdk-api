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

# ShutdownBlockReasonDestroy function


## -description


Indicates that the system can be shut down and frees the reason string.


## -parameters




### -param hWnd [in]

A handle to the main window of the application.


## -returns



If the call succeeds, the return value is nonzero.

If the call fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function can only be called from the thread that created the window specified by the <i>hWnd</i> parameter. Otherwise, the function fails and the last error code is ERROR_ACCESS_DENIED.

If system shutdown has been previously blocked by the <a href="https://msdn.microsoft.com/4c6f9159-fac2-431e-bbdf-c35c4cdb25ac">ShutdownBlockReasonCreate</a> function, this function frees the reason string. Otherwise, this function is a no-op.




## -see-also




<a href="https://msdn.microsoft.com/4c6f9159-fac2-431e-bbdf-c35c4cdb25ac">ShutdownBlockReasonCreate</a>



<a href="https://msdn.microsoft.com/acadf58f-3f68-4fa1-bdcf-8f85c8479263">Shutting Down</a>
 

 

