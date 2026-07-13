---
UID: NF:wingdi.MAKEROP4
title: MAKEROP4 macro (wingdi.h)
description: The MAKEROP4 macro creates a quaternary raster operation code for use with the MaskBlt function.
helpviewer_keywords: ["MAKEROP4","MAKEROP4 macro [Windows GDI]","_win32_MAKEROP4","gdi.makerop4","wingdi/MAKEROP4"]
old-location: gdi\makerop4.htm
tech.root: gdi
ms.assetid: 9056df62-a636-49c7-9c86-aecc731e8c4f
ms.date: 07/01/2025
ms.keywords: MAKEROP4, MAKEROP4 macro [Windows GDI], _win32_MAKEROP4, gdi.makerop4, wingdi/MAKEROP4
req.header: wingdi.h
req.include-header: Windows.h
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
 - MAKEROP4
 - wingdi/MAKEROP4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - MAKEROP4
---

# MAKEROP4 macro

## -syntax

```cpp
DWORD MAKEROP4(
    DWORD fore,
    DWORD back
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

The return value is a quaternary raster operation code for use with the <a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a> function.


## -description

The <b>MAKEROP4</b> macro creates a quaternary raster operation code for use with the <a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a> function. The macro takes two ternary raster operation codes as input, one for the foreground and one for the background, and packs their Boolean operation indexes into the high-order word of a 32-bit value. The low-order word of this value will be ignored.

## -parameters

### -param fore

The foreground ternary raster operation code.

### -param back

The background ternary raster operation code.

## -see-also

<a href="/windows/desktop/gdi/bitmap-macros">Bitmap Macros</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a>
