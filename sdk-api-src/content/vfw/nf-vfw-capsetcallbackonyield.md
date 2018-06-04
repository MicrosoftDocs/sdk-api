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

# capSetCallbackOnYield macro


## -description



The <b>capSetCallbackOnYield</b> macro sets a callback function in the application. AVICap calls this procedure when the capture window yields during streaming capture. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/d978dc3b-4336-46a4-85ae-7d588a63489b">WM_CAP_SET_CALLBACK_YIELD</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the yield callback function, of type <a href="https://msdn.microsoft.com/4d92ab5e-5cde-4fed-a661-0458b5399c2a">capYieldCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed yield callback function. 


## -remarks



Applications can optionally set a yield callback function. The yield callback function is called at least once for each video frame captured during streaming capture. If a yield callback function is installed, it will be called regardless of the state of the <b>fYield</b> member of the <a href="https://msdn.microsoft.com/6bf7e374-5991-4a7b-984a-628d3e77b2d7">CAPTUREPARMS</a> structure.

If the yield callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session. It can be disabled after streaming capture ends.

Applications typically perform some type of message processing in the callback function consisting of a <a href="http://go.microsoft.com/fwlink/p/?linkid=16992">PeekMessage</a>, <a href="http://go.microsoft.com/fwlink/p/?linkid=16993">TranslateMessage</a>, <a href="http://go.microsoft.com/fwlink/p/?linkid=16994">DispatchMessage</a> loop, as in the message loop of a <a href="http://go.microsoft.com/fwlink/p/?linkid=16995">WinMain</a> function. The yield callback function must also filter and remove messages that can cause reentrancy problems.

An application typically returns <b>TRUE</b> in the yield procedure to continue streaming capture. If a yield callback function returns <b>FALSE</b>, the capture window stops the capture process.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

