---
UID: NC:vfw.CAPWAVECALLBACK
title: CAPWAVECALLBACK
author: windows-sdk-content
description: The capWaveStreamCallback function is the callback function used with streaming capture to optionally process buffers of audio data. The name capWaveStreamCallback is a placeholder for the application-supplied function name.
old-location: multimedia\capwavestreamcallback.htm
tech.root: Multimedia
ms.assetid: e7047d3d-9393-4611-a034-d36d6e92ee01
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: CAPWAVECALLBACK, _win32_capWaveStreamCallback, capWaveStreamCallback, capWaveStreamCallback callback, capWaveStreamCallback callback function [Windows Multimedia], multimedia.capwavestreamcallback, vfw/capWaveStreamCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - UserDefined
api_location:
 - Vfw.h
api_name:
 - capWaveStreamCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

