---
UID: NF:vfw.capPalettePaste
title: capPalettePaste macro (vfw.h)
description: The capPalettePaste macro copies the palette from the clipboard and passes it to a capture driver. You can use this macro or explicitly call the WM_CAP_PAL_PASTE message.
helpviewer_keywords: ["_win32_capPalettePaste","capPalettePaste","capPalettePaste macro [Windows Multimedia]","multimedia.cappalettepaste","vfw/capPalettePaste"]
old-location: multimedia\cappalettepaste.htm
tech.root: Multimedia
ms.assetid: ccdaf58d-3d06-46c5-a812-322364a7f851
ms.date: 07/01/2025
ms.keywords: _win32_capPalettePaste, capPalettePaste, capPalettePaste macro [Windows Multimedia], multimedia.cappalettepaste, vfw/capPalettePaste
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
 - capPalettePaste
 - vfw/capPalettePaste
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
 - capPalettePaste
---

# capPalettePaste macro

## -syntax

```cpp
BOOL capPalettePaste(
     hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns **TRUE** if successful or **FALSE** otherwise.If an error occurs and an error callback function is set using the **capSetCallbackOnError** macro, the error callback function is called.


## -description

The <b>capPalettePaste</b> macro copies the palette from the clipboard and passes it to a capture driver. You can use this macro or explicitly call the <a href="/windows/desktop/Multimedia/wm-cap-pal-paste">WM_CAP_PAL_PASTE</a> message.

## -parameters

### -param hwnd

Handle to a capture window.

## -remarks

A capture driver uses a palette when required by the specified digitized video format.

## -see-also

<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
