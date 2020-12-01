---
UID: NF:wingdi.GetBitmapBits
title: GetBitmapBits function (wingdi.h)
description: The GetBitmapBits function copies the bitmap bits of a specified device-dependent bitmap into a buffer.
helpviewer_keywords: ["GetBitmapBits","GetBitmapBits function [Windows GDI]","_win32_GetBitmapBits","gdi.getbitmapbits","wingdi/GetBitmapBits"]
old-location: gdi\getbitmapbits.htm
tech.root: gdi
ms.assetid: 72e8cc6b-d282-451e-b6ec-0473d2daea7c
ms.date: 12/05/2018
ms.keywords: GetBitmapBits, GetBitmapBits function [Windows GDI], _win32_GetBitmapBits, gdi.getbitmapbits, wingdi/GetBitmapBits
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
 - GetBitmapBits
 - wingdi/GetBitmapBits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetBitmapBits
---

# GetBitmapBits function


## -description

The <b>GetBitmapBits</b> function copies the bitmap bits of a specified device-dependent bitmap into a buffer.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a> function.</div><div> </div>

## -parameters

### -param hbit [in]

A handle to the device-dependent bitmap.

### -param cb [in]

The number of bytes to copy from the bitmap into the buffer.

### -param lpvBits [out]

A pointer to a buffer to receive the bitmap bits. The bits are stored as an array of byte values.

## -returns

If the function succeeds, the return value is the number of bytes copied to the buffer.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>