---
UID: NC:vfw.CAPYIELDCALLBACK
title: CAPYIELDCALLBACK (vfw.h)
description: The capYieldCallback function is the yield callback function used with video capture. The name capYieldCallback is a placeholder for the application-supplied function name.
helpviewer_keywords: ["_win32_capYieldCallback","capYieldCallback","capYieldCallback callback","capYieldCallback callback function [Windows Multimedia]","multimedia.capyieldcallback","vfw/capYieldCallback"]
old-location: multimedia\capyieldcallback.htm
tech.root: Multimedia
ms.assetid: 4d92ab5e-5cde-4fed-a661-0458b5399c2a
ms.date: 12/05/2018
ms.keywords: _win32_capYieldCallback, capYieldCallback, capYieldCallback callback, capYieldCallback callback function [Windows Multimedia], multimedia.capyieldcallback, vfw/capYieldCallback
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
 - CAPYIELDCALLBACK
 - vfw/CAPYIELDCALLBACK
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
 - capYieldCallback
---

# CAPYIELDCALLBACK callback function


## -description

The <b>capYieldCallback</b> function is the yield callback function used with video capture. The name <b>capYieldCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-yield">WM_CAP_SET_CALLBACK_YIELD</a> message to the capture window or call the <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonyield">capSetCallbackOnYield</a> macro.

## -parameters

### -param hWnd

Handle to the capture window associated with the callback function.

## -remarks

The capture window calls the yield callback function at least once for every captured video frame, but the exact rate depends on the frame rate and the overhead of the capture driver and disk.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>