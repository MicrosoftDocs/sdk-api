---
UID: NF:vfw.capSetCallbackOnVideoStream
title: capSetCallbackOnVideoStream macro (vfw.h)
description: The capSetCallbackOnVideoStream macro sets a callback function in the application. AVICap calls this procedure during streaming capture when a video buffer is filled. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_VIDEOSTREAM message.
helpviewer_keywords: ["_win32_capSetCallbackOnVideoStream","capSetCallbackOnVideoStream","capSetCallbackOnVideoStream macro [Windows Multimedia]","multimedia.capsetcallbackonvideostream","vfw/capSetCallbackOnVideoStream"]
old-location: multimedia\capsetcallbackonvideostream.htm
tech.root: Multimedia
ms.assetid: c2e783a5-829b-4fa2-995a-c0cb4e63645b
ms.date: 07/01/2025
ms.keywords: _win32_capSetCallbackOnVideoStream, capSetCallbackOnVideoStream, capSetCallbackOnVideoStream macro [Windows Multimedia], multimedia.capsetcallbackonvideostream, vfw/capSetCallbackOnVideoStream
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
 - capSetCallbackOnVideoStream
 - vfw/capSetCallbackOnVideoStream
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
 - capSetCallbackOnVideoStream
---

# capSetCallbackOnVideoStream macro

## -syntax

```cpp
BOOL capSetCallbackOnVideoStream(
     hwnd,
     fpProc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.


## -description

The <b>capSetCallbackOnVideoStream</b> macro sets a callback function in the application. AVICap calls this procedure during streaming capture when a video buffer is filled. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-callback-videostream">WM_CAP_SET_CALLBACK_VIDEOSTREAM</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param fpProc

Pointer to the video-stream callback function, of type <a href="/windows/desktop/api/vfw/nc-vfw-capvideocallback">capVideoStreamCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed video-stream callback function.

## -remarks

The capture window calls the callback function before writing the captured frame to disk. This allows applications to modify the frame if desired.

If a video stream callback function is used for streaming capture, the procedure must be installed before starting the capture session and it must remain enabled for the duration of the session. It can be disabled after streaming capture ends.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
