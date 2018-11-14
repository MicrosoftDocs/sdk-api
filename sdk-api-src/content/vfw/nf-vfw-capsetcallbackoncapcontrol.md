---
UID: NF:vfw.capSetCallbackOnCapControl
title: capSetCallbackOnCapControl macro
author: windows-sdk-content
description: The capSetCallbackOnCapControl macro sets a callback function in the application giving it precise recording control. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_CAPCONTROL message.
old-location: multimedia\capsetcallbackoncapcontrol.htm
tech.root: Multimedia
ms.assetid: 78bc83f6-06a0-4c41-92ce-932578bcb010
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "_win32_capSetCallbackOnCapControl, capSetCallbackOnCapControl, capSetCallbackOnCapControl macro [Windows Multimedia], multimedia.capsetcallbackoncapcontrol, vfw/capSetCallbackOnCapControl"
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
 - capSetCallbackOnCapControl
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
- capSetCallbackOnCapControl
: 
---

# capSetCallbackOnCapControl macro


## -description



The <b>capSetCallbackOnCapControl</b> macro sets a callback function in the application giving it precise recording control. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/1e93ed7b-8205-45fe-bdcf-efe3f709f728">WM_CAP_SET_CALLBACK_CAPCONTROL</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the callback function, of type capControlCallback . Specify <b>NULL</b> for this parameter to disable a previously installed callback function. 


## -remarks



A single callback function is used to give the application precise control over the moments that streaming capture begins and completes. The capture window first calls the procedure with <i>nState</i> set to CONTROLCALLBACK_PREROLL after all buffers have been allocated and all other capture preparations have finished. This gives the application the ability to preroll video sources, returning from the callback function at the exact moment recording is to begin. A return value of <b>TRUE</b> from the callback function continues capture, and a return value of <b>FALSE</b> aborts capture. After capture begins, this callback function will be called frequently with <i>nState</i> set to CONTROLCALLBACK_CAPTURING to allow the application to end capture by returning <b>FALSE</b>. 




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>



<a href="https://msdn.microsoft.com/1e93ed7b-8205-45fe-bdcf-efe3f709f728">WM_CAP_SET_CALLBACK_CAPCONTROL</a>



<a href="https://msdn.microsoft.com/8e63be06-d311-4968-b436-262d9c3e9f10">capControlCallback</a>
 

 

