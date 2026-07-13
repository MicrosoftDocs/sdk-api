---
UID: NF:vfw.capCaptureSingleFrameClose
title: capCaptureSingleFrameClose macro (vfw.h)
description: The capCaptureSingleFrameClose macro closes the capture file opened by the capCaptureSingleFrameOpen macro. You can use this macro or explicitly send the WM_CAP_SINGLE_FRAME_CLOSE message.
helpviewer_keywords: ["_win32_capCaptureSingleFrameClose","capCaptureSingleFrameClose","capCaptureSingleFrameClose macro [Windows Multimedia]","multimedia.capcapturesingleframeclose","vfw/capCaptureSingleFrameClose"]
old-location: multimedia\capcapturesingleframeclose.htm
tech.root: Multimedia
ms.assetid: d0259662-6bcf-4c04-924c-e568db335fd2
ms.date: 07/01/2025
ms.keywords: _win32_capCaptureSingleFrameClose, capCaptureSingleFrameClose, capCaptureSingleFrameClose macro [Windows Multimedia], multimedia.capcapturesingleframeclose, vfw/capCaptureSingleFrameClose
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
 - capCaptureSingleFrameClose
 - vfw/capCaptureSingleFrameClose
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
 - capCaptureSingleFrameClose
---

# capCaptureSingleFrameClose macro

## -syntax

```cpp
BOOL capCaptureSingleFrameClose(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capCaptureSingleFrameClose</b> macro closes the capture file opened by the <a href="/windows/desktop/api/vfw/nf-vfw-capcapturesingleframeopen">capCaptureSingleFrameOpen</a> macro. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-single-frame-close">WM_CAP_SINGLE_FRAME_CLOSE</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

For information about installing callback functions, see the <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonerror">capSetCallbackOnError</a> and <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonframe">capSetCallbackOnFrame</a> macros.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
