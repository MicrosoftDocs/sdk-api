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

# capSetCallbackOnVideoStream macro


## -description



The <b>capSetCallbackOnVideoStream</b> macro sets a callback function in the application. AVICap calls this procedure during streaming capture when a video buffer is filled. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/590089b8-7a8d-476b-9b81-f96bf73b0369">WM_CAP_SET_CALLBACK_VIDEOSTREAM</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the video-stream callback function, of type <a href="https://msdn.microsoft.com/e21d7563-0ca8-4777-9fb0-de7c1c4ae618">capVideoStreamCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed video-stream callback function. 


## -remarks



The capture window calls the callback function before writing the captured frame to disk. This allows applications to modify the frame if desired.

If a video stream callback function is used for streaming capture, the procedure must be installed before starting the capture session and it must remain enabled for the duration of the session. It can be disabled after streaming capture ends.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

