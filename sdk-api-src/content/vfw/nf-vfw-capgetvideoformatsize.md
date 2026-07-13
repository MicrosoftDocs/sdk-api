---
UID: NF:vfw.capGetVideoFormatSize
title: capGetVideoFormatSize macro (vfw.h)
description: The capGetVideoFormatSize macro retrieves the size required for the video format. You can use this macro or explicitly call the WM_CAP_GET_VIDEOFORMAT message.
helpviewer_keywords: ["_win32_capGetVideoFormatSize","capGetVideoFormatSize","capGetVideoFormatSize macro [Windows Multimedia]","multimedia.capgetvideoformatsize","vfw/capGetVideoFormatSize"]
old-location: multimedia\capgetvideoformatsize.htm
tech.root: Multimedia
ms.assetid: 4ee78b19-4171-4da8-ad26-199067bb6db8
ms.date: 07/01/2025
ms.keywords: _win32_capGetVideoFormatSize, capGetVideoFormatSize, capGetVideoFormatSize macro [Windows Multimedia], multimedia.capgetvideoformatsize, vfw/capGetVideoFormatSize
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
 - capGetVideoFormatSize
 - vfw/capGetVideoFormatSize
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
 - capGetVideoFormatSize
---

# capGetVideoFormatSize macro

## -syntax

```cpp
DWORD capGetVideoFormatSize(
     hwnd
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the size, in bytes, of the video format or zero if the capture window is not connected to a capture driver. For video formats that require a palette, the current palette is also returned.


## -description

The <b>capGetVideoFormatSize</b> macro retrieves the size required for the video format. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-get-videoformat">WM_CAP_GET_VIDEOFORMAT</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
