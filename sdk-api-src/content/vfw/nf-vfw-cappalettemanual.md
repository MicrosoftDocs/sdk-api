---
UID: NF:vfw.capPaletteManual
title: capPaletteManual macro (vfw.h)
description: The capPaletteManual macro requests that the capture driver manually sample video frames and create a new palette. You can use this macro or explicitly call the WM_CAP_PAL_MANUALCREATE message.
helpviewer_keywords: ["_win32_capPaletteManual","capPaletteManual","capPaletteManual macro [Windows Multimedia]","multimedia.cappalettemanual","vfw/capPaletteManual"]
old-location: multimedia\cappalettemanual.htm
tech.root: Multimedia
ms.assetid: 81dc204a-36a5-45eb-8c29-a6004d3cd49c
ms.date: 07/01/2025
ms.keywords: _win32_capPaletteManual, capPaletteManual, capPaletteManual macro [Windows Multimedia], multimedia.cappalettemanual, vfw/capPaletteManual
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
 - capPaletteManual
 - vfw/capPaletteManual
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
 - capPaletteManual
---

# capPaletteManual macro

## -syntax

```cpp
BOOL capPaletteManual(
     hwnd,
     fGrab,
     iColors
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.If an error occurs and an error callback function is set using the **capSetCallbackOnError** macro, the error callback function is called.


## -description

The <b>capPaletteManual</b> macro requests that the capture driver manually sample video frames and create a new palette. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-pal-manualcreate">WM_CAP_PAL_MANUALCREATE</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param fGrab

Palette histogram flag. Set this parameter to <b>TRUE</b> for each frame included in creating the optimal palette. After the last frame has been collected, set this parameter to <b>FALSE</b> to calculate the optimal palette and send it to the capture driver.

### -param iColors

Number of colors in the palette. The maximum value for this parameter is 256. This value is used only during collection of the first frame in a sequence.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
