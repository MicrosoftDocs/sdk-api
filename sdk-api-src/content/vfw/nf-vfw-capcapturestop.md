---
UID: NF:vfw.capCaptureStop
title: capCaptureStop macro (vfw.h)
description: The capCaptureStop macro stops the capture operation. You can use this macro or explicitly send the WM_CAP_STOP message.
helpviewer_keywords: ["_win32_capCaptureStop","capCaptureStop","capCaptureStop macro [Windows Multimedia]","multimedia.capcapturestop","vfw/capCaptureStop"]
old-location: multimedia\capcapturestop.htm
tech.root: Multimedia
ms.assetid: 79b33f36-1bf9-41f2-827f-d0cfa276113e
ms.date: 07/01/2025
ms.keywords: _win32_capCaptureStop, capCaptureStop, capCaptureStop macro [Windows Multimedia], multimedia.capcapturestop, vfw/capCaptureStop
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
 - capCaptureStop
 - vfw/capCaptureStop
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
 - capCaptureStop
---

# capCaptureStop macro

## -syntax

```cpp
BOOL capCaptureStop(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capCaptureStop</b> macro stops the capture operation. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-stop">WM_CAP_STOP</a> message.



In step frame capture, the image data that was collected before this message was sent is retained in the capture file. An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

The capture operation must yield to use this message. Use the <a href="/windows/desktop/api/vfw/nf-vfw-capcaptureabort">capCaptureAbort</a> macro to abandon the current capture operation.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
