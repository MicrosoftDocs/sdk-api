---
UID: NF:vfw.capSetCallbackOnYield
title: capSetCallbackOnYield macro
author: windows-sdk-content
description: The capSetCallbackOnYield macro sets a callback function in the application. AVICap calls this procedure when the capture window yields during streaming capture. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_YIELD message.
old-location: multimedia\capsetcallbackonyield.htm
tech.root: Multimedia
ms.assetid: efddbcbc-f1e3-451c-928e-984eea187de2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_win32_capSetCallbackOnYield, capSetCallbackOnYield, capSetCallbackOnYield macro [Windows Multimedia], multimedia.capsetcallbackonyield, vfw/capSetCallbackOnYield"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - capSetCallbackOnYield
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- vfw.h
: 
- capSetCallbackOnYield
: 
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
 

 

