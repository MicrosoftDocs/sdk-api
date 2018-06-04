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

# capCaptureAbort macro


## -description



The <b>capCaptureAbort</b> macro stops the capture operation. You can use this macro or explictly send the <a href="https://msdn.microsoft.com/a0479d73-8422-4833-9e8a-c262ec386f58">WM_CAP_ABORT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



The capture operation must yield to use this macro.

In the case of step capture, the image data collected up to the point of the <b>capCaptureAbort</b> macro will be retained in the capture file, but audio will not be captured.

Use the <a href="https://msdn.microsoft.com/79b33f36-1bf9-41f2-827f-d0cfa276113e">capCaptureStop</a> macro to halt step capture at the current position, and then capture audio.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>



<a href="https://msdn.microsoft.com/79b33f36-1bf9-41f2-827f-d0cfa276113e">capCaptureStop</a>
 

 

