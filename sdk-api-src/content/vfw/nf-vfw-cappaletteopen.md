---
UID: NF:vfw.capPaletteOpen
title: capPaletteOpen macro (vfw.h)
description: The capPaletteOpen macro loads a new palette from a palette file and passes it to a capture driver.
helpviewer_keywords: ["_win32_capPaletteOpen","capPaletteOpen","capPaletteOpen macro [Windows Multimedia]","multimedia.cappaletteopen","vfw/capPaletteOpen"]
old-location: multimedia\cappaletteopen.htm
tech.root: Multimedia
ms.assetid: 1d50795e-c414-4bf5-a255-76532a34d944
ms.date: 07/01/2025
ms.keywords: _win32_capPaletteOpen, capPaletteOpen, capPaletteOpen macro [Windows Multimedia], multimedia.cappaletteopen, vfw/capPaletteOpen
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
 - capPaletteOpen
 - vfw/capPaletteOpen
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
 - capPaletteOpen
---

# capPaletteOpen macro

## -syntax

```cpp
BOOL capPaletteOpen(
     hwnd,
     szName
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.If an error occurs and an error callback function is set using the **capSetCallbackOnError** macro, the error callback function is called.


## -description

The <b>capPaletteOpen</b> macro loads a new palette from a palette file and passes it to a capture driver. Palette files typically use the filename extension .PAL. A capture driver uses a palette when required by the specified digitized image format. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-pal-open">WM_CAP_PAL_OPEN</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

### -param szName

Pointer to a null-terminated string containing the palette filename.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
