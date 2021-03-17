---
UID: NC:vfw.CAPCONTROLCALLBACK
title: CAPCONTROLCALLBACK (vfw.h)
description: The capControlCallback function is the callback function used for precision control to begin and end streaming capture. The name capControlCallback is a placeholder for the application-supplied function name.
helpviewer_keywords: ["_win32_capControlCallback","capControlCallback","capControlCallback callback","capControlCallback callback function [Windows Multimedia]","multimedia.capcontrolcallback","vfw/capControlCallback"]
old-location: multimedia\capcontrolcallback.htm
tech.root: Multimedia
ms.assetid: 8e63be06-d311-4968-b436-262d9c3e9f10
ms.date: 12/05/2018
ms.keywords: _win32_capControlCallback, capControlCallback, capControlCallback callback, capControlCallback callback function [Windows Multimedia], multimedia.capcontrolcallback, vfw/capControlCallback
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
 - CAPCONTROLCALLBACK
 - vfw/CAPCONTROLCALLBACK
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
 - capControlCallback
---

# CAPCONTROLCALLBACK callback function


## -description

The <b>capControlCallback</b> function is the callback function used for precision control to begin and end streaming capture. The name <b>capControlCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-capcontrol">WM_CAP_SET_CALLBACK_CAPCONTROL</a> message to the capture window or call the <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackoncapcontrol">capSetCallbackOnCapControl</a> macro.

## -parameters

### -param hWnd

Handle to the capture window associated with the callback function.

### -param nState

Current state of the capture operation. The CONTROLCALLBACK_PREROLL value is sent initially to enable prerolling of the video sources and to return control to the capture application at the exact moment recording is to begin. The CONTROLCALLBACK_CAPTURING value is sent once per captured frame to indicate that streaming capture is in progress and to enable the application to end capture.

## -returns

When <i>nState</i> is set to CONTROLCALLBACK_PREROLL, this callback function must return <b>TRUE</b> to start capture or <b>FALSE</b> to abort it. When <i>nState</i> is set to CONTROLCALLBACK_CAPTURING, this callback function must return <b>TRUE</b> to continue capture or <b>FALSE</b> to end it.

## -remarks

The first message sent to the callback procedure sets the <i>nState</i> parameter to CONTROLCALLBACK_PREROLL after allocating all buffers and all other capture preparations are complete.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>