---
UID: NC:vfw.CAPWAVECALLBACK
title: CAPWAVECALLBACK (vfw.h)
description: The capWaveStreamCallback function is the callback function used with streaming capture to optionally process buffers of audio data. The name capWaveStreamCallback is a placeholder for the application-supplied function name.
helpviewer_keywords: ["CAPWAVECALLBACK","_win32_capWaveStreamCallback","capWaveStreamCallback","capWaveStreamCallback callback","capWaveStreamCallback callback function [Windows Multimedia]","multimedia.capwavestreamcallback","vfw/capWaveStreamCallback"]
old-location: multimedia\capwavestreamcallback.htm
tech.root: Multimedia
ms.assetid: e7047d3d-9393-4611-a034-d36d6e92ee01
ms.date: 12/05/2018
ms.keywords: CAPWAVECALLBACK, _win32_capWaveStreamCallback, capWaveStreamCallback, capWaveStreamCallback callback, capWaveStreamCallback callback function [Windows Multimedia], multimedia.capwavestreamcallback, vfw/capWaveStreamCallback
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
 - CAPWAVECALLBACK
 - vfw/CAPWAVECALLBACK
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
 - capWaveStreamCallback
---

# CAPWAVECALLBACK callback function


## -description

The <b>capWaveStreamCallback</b> function is the callback function used with streaming capture to optionally process buffers of audio data. The name <b>capWaveStreamCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-wavestream">WM_CAP_SET_CALLBACK_WAVESTREAM</a> message to the capture window or call the <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonwavestream">capSetCallbackOnWaveStream</a> macro.

## -parameters

### -param hWnd

Handle to the capture window associated with the callback function.

### -param lpWHdr

Pointer to a <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure containing information about the captured audio data.

## -remarks

The capture window calls a wave stream callback function when an audio buffer is marked done by the waveform-audio driver. When capturing to disk, this will precede the disk write operation.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>