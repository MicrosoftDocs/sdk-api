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

# capCaptureStop macro


## -description



The <b>capCaptureStop</b> macro stops the capture operation. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/0fea82f5-f381-485a-82ae-b081b3a5e402">WM_CAP_STOP</a> message.



In step frame capture, the image data that was collected before this message was sent is retained in the capture file. An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.


## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



The capture operation must yield to use this message. Use the <a href="https://msdn.microsoft.com/a1c17695-ee91-4f76-a2be-a6e512903c8f">capCaptureAbort</a> macro to abandon the current capture operation.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

