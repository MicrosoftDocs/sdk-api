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
 

 

