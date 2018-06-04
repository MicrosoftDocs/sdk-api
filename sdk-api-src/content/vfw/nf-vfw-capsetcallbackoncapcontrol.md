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
 

 

