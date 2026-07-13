---
UID: NF:vfw.capCaptureAbort
title: capCaptureAbort macro (vfw.h)
description: The capCaptureAbort macro stops the capture operation. You can use this macro or explicitly send the WM_CAP_ABORT message.
helpviewer_keywords: ["_win32_capCaptureAbort","capCaptureAbort","capCaptureAbort macro [Windows Multimedia]","multimedia.capcaptureabort","vfw/capCaptureAbort"]
old-location: multimedia\capcaptureabort.htm
tech.root: Multimedia
ms.assetid: a1c17695-ee91-4f76-a2be-a6e512903c8f
ms.date: 07/01/2025
ms.keywords: _win32_capCaptureAbort, capCaptureAbort, capCaptureAbort macro [Windows Multimedia], multimedia.capcaptureabort, vfw/capCaptureAbort
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
 - capCaptureAbort
 - vfw/capCaptureAbort
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
 - capCaptureAbort
---

# capCaptureAbort macro

## -syntax

```cpp
BOOL capCaptureAbort(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capCaptureAbort</b> macro stops the capture operation. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-abort">WM_CAP_ABORT</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

The capture operation must yield to use this macro.

In the case of step capture, the image data collected up to the point of the <b>capCaptureAbort</b> macro will be retained in the capture file, but audio will not be captured.

Use the <a href="/windows/desktop/api/vfw/nf-vfw-capcapturestop">capCaptureStop</a> macro to halt step capture at the current position, and then capture audio.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>



<a href="/windows/desktop/api/vfw/nf-vfw-capcapturestop">capCaptureStop</a>
