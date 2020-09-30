---
UID: NF:wingdi.SetBitmapBits
title: SetBitmapBits function (wingdi.h)
description: The SetBitmapBits function sets the bits of color data for a bitmap to the specified values.
helpviewer_keywords: ["SetBitmapBits","SetBitmapBits function [Windows GDI]","_win32_SetBitmapBits","gdi.setbitmapbits","wingdi/SetBitmapBits"]
old-location: gdi\setbitmapbits.htm
tech.root: gdi
ms.assetid: 3cab12a6-c408-4552-bec0-5ecfd8374757
ms.date: 12/05/2018
ms.keywords: SetBitmapBits, SetBitmapBits function [Windows GDI], _win32_SetBitmapBits, gdi.setbitmapbits, wingdi/SetBitmapBits
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetBitmapBits
 - wingdi/SetBitmapBits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetBitmapBits
---

# SetBitmapBits function


## -description

The <b>SetBitmapBits</b> function sets the bits of color data for a bitmap to the specified values.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> function.</div><div> </div>

## -parameters

### -param hbm [in]

A handle to the bitmap to be set. This must be a compatible bitmap (DDB).

### -param cb [in]

The number of bytes pointed to by the <i>lpBits</i> parameter.

### -param pvBits [in]

A pointer to an array of bytes that contain color data for the specified bitmap.

## -returns

If the function succeeds, the return value is the number of bytes used in setting the bitmap bits.

If the function fails, the return value is zero.

## -remarks

The array identified by <i>lpBits</i> must be WORD aligned.

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbitmapbits">GetBitmapBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>