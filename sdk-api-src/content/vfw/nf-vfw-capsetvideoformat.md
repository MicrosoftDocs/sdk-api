---
UID: NF:vfw.capSetVideoFormat
title: capSetVideoFormat macro (vfw.h)
description: The capSetVideoFormat macro sets the format of captured video data. You can use this macro or explicitly call the WM_CAP_SET_VIDEOFORMAT message.
helpviewer_keywords: ["_win32_capSetVideoFormat","capSetVideoFormat","capSetVideoFormat macro [Windows Multimedia]","multimedia.capsetvideoformat","vfw/capSetVideoFormat"]
old-location: multimedia\capsetvideoformat.htm
tech.root: Multimedia
ms.assetid: 3c4bee26-d578-463b-8d97-6cdc78957ce0
ms.date: 07/01/2025
ms.keywords: _win32_capSetVideoFormat, capSetVideoFormat, capSetVideoFormat macro [Windows Multimedia], multimedia.capsetvideoformat, vfw/capSetVideoFormat
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
 - capSetVideoFormat
 - vfw/capSetVideoFormat
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
 - capSetVideoFormat
---

# capSetVideoFormat macro

## -syntax

```cpp
BOOL capSetVideoFormat(
     hwnd,
     s,
     wSize
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.


## -description

The <b>capSetVideoFormat</b> macro sets the format of captured video data. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-set-videoformat">WM_CAP_SET_VIDEOFORMAT</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param s

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

### -param wSize

The size, in bytes, of the structure referenced by <i>psVideoFormat</i>.

## -remarks

Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
