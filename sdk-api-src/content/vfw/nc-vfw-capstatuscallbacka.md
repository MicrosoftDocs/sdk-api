---
UID: NC:vfw.CAPSTATUSCALLBACKA
title: CAPSTATUSCALLBACKA (vfw.h)
description: The capStatusCallback function is the status callback function used with video capture. The name capStatusCallback is a placeholder for the application-supplied function name. (ANSI)
helpviewer_keywords: ["CAPSTATUSCALLBACKA","CAPSTATUSCALLBACKW","_win32_capStatusCallback","capStatusCallback","capStatusCallback callback","capStatusCallback callback function [Windows Multimedia]","multimedia.capstatuscallback","vfw/CAPSTATUSCALLBACKA","vfw/CAPSTATUSCALLBACKW","vfw/capStatusCallback"]
old-location: multimedia\capstatuscallback.htm
tech.root: Multimedia
ms.assetid: b48021a7-7fa1-4837-a6ca-af266fd55f4f
ms.date: 12/05/2018
ms.keywords: CAPSTATUSCALLBACKA, CAPSTATUSCALLBACKW, _win32_capStatusCallback, capStatusCallback, capStatusCallback callback, capStatusCallback callback function [Windows Multimedia], multimedia.capstatuscallback, vfw/CAPSTATUSCALLBACKA, vfw/CAPSTATUSCALLBACKW, vfw/capStatusCallback
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CAPSTATUSCALLBACKW (Unicode) and CAPSTATUSCALLBACKA (ANSI)
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
 - CAPSTATUSCALLBACKA
 - vfw/CAPSTATUSCALLBACKA
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
 - capStatusCallback
 - CAPSTATUSCALLBACKA
 - CAPSTATUSCALLBACKW
---

# CAPSTATUSCALLBACKA callback function


## -description

The <b>capStatusCallback</b> function is the status callback function used with video capture. The name <b>capStatusCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-status">WM_CAP_SET_CALLBACK_STATUS</a> message to the capture window or call the <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonstatus">capSetCallbackOnStatus</a> macro.

## -parameters

### -param hWnd

Handle to the capture window associated with the callback function.

### -param nID

Message identification number.

### -param lpsz

Pointer to a textual description of the returned status.

## -remarks

During capture operations, the first message sent to the callback function is always IDS_CAP_BEGIN and the last is always IDS_CAP_END. A message identifier of zero indicates a new operation is starting and the callback function should clear the current status.





> [!NOTE]
> The vfw.h header defines CAPSTATUSCALLBACK as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>
