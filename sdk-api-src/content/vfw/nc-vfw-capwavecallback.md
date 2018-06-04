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

# CAPWAVECALLBACK callback function


## -description



The <b>capWaveStreamCallback</b> function is the callback function used with streaming capture to optionally process buffers of audio data. The name <b>capWaveStreamCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="https://msdn.microsoft.com/f2554cbb-73de-4f76-b785-6c18c82c2992">WM_CAP_SET_CALLBACK_WAVESTREAM</a> message to the capture window or call the <a href="https://msdn.microsoft.com/282386af-506b-4be6-bb75-aa3c62f9778a">capSetCallbackOnWaveStream</a> macro.


## -parameters




### -param hWnd

Handle to the capture window associated with the callback function.


### -param lpWHdr

Pointer to a <a href="https://msdn.microsoft.com/be70ae8e-8d8f-4261-bd0e-c6fd7feec520">WAVEHDR</a> structure containing information about the captured audio data.


## -remarks



The capture window calls a wave stream callback function when an audio buffer is marked done by the waveform-audio driver. When capturing to disk, this will precede the disk write operation.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

