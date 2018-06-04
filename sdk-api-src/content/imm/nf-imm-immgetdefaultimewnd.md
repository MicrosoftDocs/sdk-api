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

# ImmGetDefaultIMEWnd function


## -description


Retrieves the default window handle to the IME class.


## -parameters




### -param HWND

TBD




#### - hWnd [in]

Handle to the window.


## -returns



Returns the default window handle to the IME class if successful, or <b>NULL</b> otherwise.




## -remarks



The operating system creates a default IME window for every thread. The window is created based on the IME class. The application can send the <a href="https://msdn.microsoft.com/5d3b7f8a-57c9-41e3-8022-9a3f515fc32e">WM_IME_CONTROL</a> message to this window.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>



<a href="https://msdn.microsoft.com/5d3b7f8a-57c9-41e3-8022-9a3f515fc32e">WM_IME_CONTROL</a>
 

 

