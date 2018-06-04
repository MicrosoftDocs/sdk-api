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

# CAPCONTROLCALLBACK callback function


## -description



The <b>capControlCallback</b> function is the callback function used for precision control to begin and end streaming capture. The name <b>capControlCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="https://msdn.microsoft.com/1e93ed7b-8205-45fe-bdcf-efe3f709f728">WM_CAP_SET_CALLBACK_CAPCONTROL</a> message to the capture window or call the <a href="https://msdn.microsoft.com/78bc83f6-06a0-4c41-92ce-932578bcb010">capSetCallbackOnCapControl</a> macro.


## -parameters




### -param hWnd

Handle to the capture window associated with the callback function.


### -param nState

Current state of the capture operation. The CONTROLCALLBACK_PREROLL value is sent initially to enable prerolling of the video sources and to return control to the capture application at the exact moment recording is to begin. The CONTROLCALLBACK_CAPTURING value is sent once per captured frame to indicate that streaming capture is in progress and to enable the application to end capture.


## -returns



When <i>nState</i> is set to CONTROLCALLBACK_PREROLL, this callback function must return <b>TRUE</b> to start capture or <b>FALSE</b> to abort it. When <i>nState</i> is set to CONTROLCALLBACK_CAPTURING, this callback function must return <b>TRUE</b> to continue capture or <b>FALSE</b> to end it.




## -remarks



The first message sent to the callback procedure sets the <i>nState</i> parameter to CONTROLCALLBACK_PREROLL after allocating all buffers and all other capture preparations are complete.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

