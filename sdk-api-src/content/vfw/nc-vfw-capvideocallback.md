---
UID: NC:vfw.CAPVIDEOCALLBACK
title: CAPVIDEOCALLBACK
author: windows-sdk-content
description: The capVideoStreamCallback function is the callback function used with streaming capture to optionally process a frame of captured video. The name capVideoStreamCallback is a placeholder for the application-supplied function name.
old-location: multimedia\capvideostreamcallback.htm
tech.root: Multimedia
ms.assetid: e21d7563-0ca8-4777-9fb0-de7c1c4ae618
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CAPVIDEOCALLBACK, _win32_capVideoStreamCallback, capVideoStreamCallback, capVideoStreamCallback callback, capVideoStreamCallback callback function [Windows Multimedia], multimedia.capvideostreamcallback, vfw/capVideoStreamCallback
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
 - capVideoStreamCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CAPVIDEOCALLBACK callback function


## -description



The <b>capVideoStreamCallback</b> function is the callback function used with streaming capture to optionally process a frame of captured video. The name <b>capVideoStreamCallback</b> is a placeholder for the application-supplied function name.



To set this callback for streaming capture, send the <a href="https://msdn.microsoft.com/590089b8-7a8d-476b-9b81-f96bf73b0369">WM_CAP_SET_CALLBACK_VIDEOSTREAM</a> message to the capture window or call the <a href="https://msdn.microsoft.com/c2e783a5-829b-4fa2-995a-c0cb4e63645b">capSetCallbackOnVideoStream</a> macro.

To set this callback for preview frame capture, send the <a href="https://msdn.microsoft.com/3882e6f6-c48c-4e50-9697-cbdf5b9342a5">WM_CAP_SET_CALLBACK_FRAME</a> message to the capture window or call the <a href="https://msdn.microsoft.com/7e9e33cb-9213-4111-a1de-700493949f2d">capSetCallbackOnFrame</a> macro.


## -parameters




### -param hWnd

Handle to the capture window associated with the callback function.


### -param lpVHdr

Pointer to a <a href="https://msdn.microsoft.com/81e4dded-7ba1-40cf-bc16-20524b70a28d">VIDEOHDR</a> structure containing information about the captured frame.


## -remarks



The capture window calls a video stream callback function when a video buffer is marked done by the capture driver. When capturing to disk, this will precede the disk write operation.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

