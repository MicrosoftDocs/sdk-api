---
UID: NF:vfw.capCaptureSingleFrame
title: capCaptureSingleFrame macro (vfw.h)
description: The capCaptureSingleFrame macro appends a single frame to a capture file that was opened using the capCaptureSingleFrameOpen macro. You can use this macro or explicitly send the WM_CAP_SINGLE_FRAME message.
helpviewer_keywords: ["_win32_capCaptureSingleFrame","capCaptureSingleFrame","capCaptureSingleFrame macro [Windows Multimedia]","multimedia.capcapturesingleframe","vfw/capCaptureSingleFrame"]
old-location: multimedia\capcapturesingleframe.htm
tech.root: Multimedia
ms.assetid: 1204cd8f-a439-4dcc-8bba-f8fbc2184ca4
ms.date: 07/01/2025
ms.keywords: _win32_capCaptureSingleFrame, capCaptureSingleFrame, capCaptureSingleFrame macro [Windows Multimedia], multimedia.capcapturesingleframe, vfw/capCaptureSingleFrame
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
 - capCaptureSingleFrame
 - vfw/capCaptureSingleFrame
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
 - capCaptureSingleFrame
---

# capCaptureSingleFrame macro

## -syntax

```cpp
BOOL capCaptureSingleFrame(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capCaptureSingleFrame</b> macro appends a single frame to a capture file that was opened using the <a href="/windows/desktop/api/vfw/nf-vfw-capcapturesingleframeopen">capCaptureSingleFrameOpen</a> macro. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/wm-cap-single-frame">WM_CAP_SINGLE_FRAME</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
