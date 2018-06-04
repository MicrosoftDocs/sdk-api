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

# ImmGetVirtualKey function


## -description


Retrieves the original virtual key value associated with a key input message that the IME has already processed.


## -parameters




### -param HWND

TBD




#### - hWnd [in]

Handle to the window that receives the key message.


## -returns



If <a href="_win32_TranslateMessage">TranslateMessage</a> has been called by the application, <b>ImmGetVirtualKey</b> returns VK_PROCESSKEY; otherwise, it returns the virtual key.




## -remarks



Although the IME sets the virtual key value to VK_PROCESSKEY after processing a key input message, an application can recover the original virtual key value with the <b>ImmGetVirtualKey</b> function. This function is used only for key input messages containing the VK_PROCESSKEY value. Applications can only get the original virtual key by using this function after receiving 

the <a href="_win32_WM_KEYDOWN">WM_KEYDOWN</a> (VK_PROCESSKEY) message, and before <a href="_win32_TranslateMessage">TranslateMessage</a> is called in its own 

message loop.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

