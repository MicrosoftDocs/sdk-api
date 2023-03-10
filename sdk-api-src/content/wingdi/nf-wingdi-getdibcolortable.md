---
UID: NF:wingdi.GetDIBColorTable
title: GetDIBColorTable function (wingdi.h)
description: The GetDIBColorTable function retrieves RGB (red, green, blue) color values from a range of entries in the color table of the DIB section bitmap that is currently selected into a specified device context.
helpviewer_keywords: ["GetDIBColorTable","GetDIBColorTable function [Windows GDI]","_win32_GetDIBColorTable","gdi.getdibcolortable","wingdi/GetDIBColorTable"]
old-location: gdi\getdibcolortable.htm
tech.root: gdi
ms.assetid: 3e3319be-8a3d-4ac2-ba36-9dbf18243472
ms.date: 12/05/2018
ms.keywords: GetDIBColorTable, GetDIBColorTable function [Windows GDI], _win32_GetDIBColorTable, gdi.getdibcolortable, wingdi/GetDIBColorTable
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
 - GetDIBColorTable
 - wingdi/GetDIBColorTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-L1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetDIBColorTable
---

# GetDIBColorTable function


## -description

The <b>GetDIBColorTable</b> function retrieves RGB (red, green, blue) color values from a range of entries in the color table of the DIB section bitmap that is currently selected into a specified device context.

## -parameters

### -param hdc [in]

A handle to a device context. A DIB section bitmap must be selected into this device context.

### -param iStart [in]

A zero-based color table index that specifies the first color table entry to retrieve.

### -param cEntries [in]

The number of color table entries to retrieve.

### -param prgbq [out]

A pointer to a buffer that receives an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a> data structures containing color information from the DIB color table. The buffer must be large enough to contain as many <b>RGBQUAD</b> data structures as the value of <i>cEntries</i>.

## -returns

If the function succeeds, the return value is the number of color table entries that the function retrieves.

If the function fails, the return value is zero.

## -remarks

The <b>GetDIBColorTable</b> function should be called to retrieve the color table for DIB section bitmaps that use 1, 4, or 8 bpp. The <b>biBitCount</b> member of a bitmap associated <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure specifies the number of bits-per-pixel. DIB section bitmaps with a <b>biBitCount</b> value greater than eight do not have a color table, but they do have associated color masks. Call the <a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a> function to retrieve those color masks.

## -see-also

<a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibcolortable">SetDIBColorTable</a>