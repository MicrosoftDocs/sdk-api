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

# ImmGetContext function


## -description


Returns the input context associated with the specified window.


## -parameters




### -param HWND

TBD




#### - hWnd [in]

Handle to the window for which to retrieve the input context.


## -returns



Returns the handle to the input context.




## -remarks



An application should routinely use this function to retrieve the current input context before attempting to access information in the context.

The application must call <a href="https://msdn.microsoft.com/e14b087a-58ef-4360-9368-3fdd088c14f6">ImmReleaseContext</a> when it is finished with the input context.




## -see-also




<a href="https://msdn.microsoft.com/e14b087a-58ef-4360-9368-3fdd088c14f6">ImmReleaseContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

