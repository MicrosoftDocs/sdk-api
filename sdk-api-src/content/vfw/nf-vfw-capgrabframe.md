---
UID: NF:vfw.capGrabFrame
title: capGrabFrame macro (vfw.h)
description: The capGrabFrame macro retrieves and displays a single frame from the capture driver. After capture, overlay and preview are disabled. You can use this macro or explicitly call the WM_CAP_GRAB_FRAME message.
helpviewer_keywords: ["_win32_capGrabFrame","capGrabFrame","capGrabFrame macro [Windows Multimedia]","multimedia.capgrabframe","vfw/capGrabFrame"]
old-location: multimedia\capgrabframe.htm
tech.root: Multimedia
ms.assetid: bd306414-74a9-4683-ad63-797a37152e8f
ms.date: 07/01/2025
ms.keywords: _win32_capGrabFrame, capGrabFrame, capGrabFrame macro [Windows Multimedia], multimedia.capgrabframe, vfw/capGrabFrame
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
 - capGrabFrame
 - vfw/capGrabFrame
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
 - capGrabFrame
---

# capGrabFrame macro

## -syntax

```cpp
BOOL capGrabFrame(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capGrabFrame</b> macro retrieves and displays a single frame from the capture driver. After capture, overlay and preview are disabled. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-grab-frame">WM_CAP_GRAB_FRAME</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

For information about installing callback functions, see the <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonerror">capSetCallbackOnError</a> and <a href="/windows/desktop/api/vfw/nf-vfw-capsetcallbackonframe">capSetCallbackOnFrame</a> macros.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
