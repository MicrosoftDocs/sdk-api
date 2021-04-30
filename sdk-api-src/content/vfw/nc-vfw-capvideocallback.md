---
UID: NC:vfw.CAPVIDEOCALLBACK
title: CAPVIDEOCALLBACK (vfw.h)
description: The capVideoStreamCallback function is the callback function used with streaming capture to optionally process a frame of captured video. The name capVideoStreamCallback is a placeholder for the application-supplied function name.
helpviewer_keywords: ["CAPVIDEOCALLBACK","_win32_capVideoStreamCallback","capVideoStreamCallback","capVideoStreamCallback callback","capVideoStreamCallback callback function [Windows Multimedia]","multimedia.capvideostreamcallback","vfw/capVideoStreamCallback"]
old-location: multimedia\capvideostreamcallback.htm
tech.root: Multimedia
ms.assetid: e21d7563-0ca8-4777-9fb0-de7c1c4ae618
ms.date: 12/05/2018
ms.keywords: CAPVIDEOCALLBACK, _win32_capVideoStreamCallback, capVideoStreamCallback, capVideoStreamCallback callback, capVideoStreamCallback callback function [Windows Multimedia], multimedia.capvideostreamcallback, vfw/capVideoStreamCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CAPVIDEOCALLBACK
 - vfw/CAPVIDEOCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Vfw.h
api_name:
 - capVideoStreamCallback
---

# CAPVIDEOCALLBACK callback function


## -description

The <b>capVideoStreamCallback</b> function is the callback function used with streaming capture to optionally process a frame of captured video. The name <b>capVideoStreamCallback</b> is a placeholder for the application-supplied function name.



To set this callback for streaming capture, send the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-videostream">WM_CAP_SET_CALLBACK_VIDEOSTREAM</a> message to the capture window or call the <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonvideostream">capSetCallbackOnVideoStream</a> macro.

To set this callback for preview frame capture, send the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-frame">WM_CAP_SET_CALLBACK_FRAME</a> message to the capture window or call the <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonframe">capSetCallbackOnFrame</a> macro.

## -parameters

### -param hWnd

Handle to the capture window associated with the callback function.

### -param lpVHdr

Pointer to a <a href="/windows/desktop/api/vfw/ns-vfw-videohdr">VIDEOHDR</a> structure containing information about the captured frame.

## -remarks

The capture window calls a video stream callback function when a video buffer is marked done by the capture driver. When capturing to disk, this will precede the disk write operation.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>