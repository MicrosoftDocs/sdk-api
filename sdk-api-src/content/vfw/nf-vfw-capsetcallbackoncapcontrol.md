---
UID: NF:vfw.capSetCallbackOnCapControl
title: capSetCallbackOnCapControl macro (vfw.h)
description: The capSetCallbackOnCapControl macro sets a callback function in the application giving it precise recording control. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_CAPCONTROL message.
helpviewer_keywords: ["_win32_capSetCallbackOnCapControl","capSetCallbackOnCapControl","capSetCallbackOnCapControl macro [Windows Multimedia]","multimedia.capsetcallbackoncapcontrol","vfw/capSetCallbackOnCapControl"]
old-location: multimedia\capsetcallbackoncapcontrol.htm
tech.root: Multimedia
ms.assetid: 78bc83f6-06a0-4c41-92ce-932578bcb010
ms.date: 07/01/2025
ms.keywords: _win32_capSetCallbackOnCapControl, capSetCallbackOnCapControl, capSetCallbackOnCapControl macro [Windows Multimedia], multimedia.capsetcallbackoncapcontrol, vfw/capSetCallbackOnCapControl
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
 - capSetCallbackOnCapControl
 - vfw/capSetCallbackOnCapControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - capSetCallbackOnCapControl
---

# capSetCallbackOnCapControl macro

## -syntax

```cpp
BOOL capSetCallbackOnCapControl(
     hwnd,
     fpProc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.


## -description

The <b>capSetCallbackOnCapControl</b> macro sets a callback function in the application giving it precise recording control. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-capcontrol">WM_CAP_SET_CALLBACK_CAPCONTROL</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param fpProc

Pointer to the callback function, of type capControlCallback . Specify <b>NULL</b> for this parameter to disable a previously installed callback function.

## -remarks

A single callback function is used to give the application precise control over the moments that streaming capture begins and completes. The capture window first calls the procedure with <i>nState</i> set to CONTROLCALLBACK_PREROLL after all buffers have been allocated and all other capture preparations have finished. This gives the application the ability to preroll video sources, returning from the callback function at the exact moment recording is to begin. A return value of <b>TRUE</b> from the callback function continues capture, and a return value of <b>FALSE</b> aborts capture. After capture begins, this callback function will be called frequently with <i>nState</i> set to CONTROLCALLBACK_CAPTURING to allow the application to end capture by returning <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>



<a href="/windows/desktop/Multimedia/wm-cap-set-callback-capcontrol">WM_CAP_SET_CALLBACK_CAPCONTROL</a>



<a href="/windows/desktop/api/vfw/nc-vfw-capcontrolcallback">capControlCallback</a>
