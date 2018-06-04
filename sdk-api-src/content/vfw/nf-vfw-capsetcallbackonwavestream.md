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

# capSetCallbackOnWaveStream macro


## -description



The <b>capSetCallbackOnWaveStream</b> macro sets a callback function in the application. AVICap calls this procedure during streaming capture when a new audio buffer becomes available. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/f2554cbb-73de-4f76-b785-6c18c82c2992">WM_CAP_SET_CALLBACK_WAVESTREAM</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the wave stream callback function, of type <a href="https://msdn.microsoft.com/e7047d3d-9393-4611-a034-d36d6e92ee01">capWaveStreamCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed wave stream callback function. 


## -remarks



The capture window calls the procedure before writing the audio buffer to disk. This allows applications to modify the audio buffer if desired.

If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session. It can be disabled after streaming capture ends.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

