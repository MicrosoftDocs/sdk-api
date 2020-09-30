---
UID: NF:wingdi.CreatePatternBrush
title: CreatePatternBrush function (wingdi.h)
description: The CreatePatternBrush function creates a logical brush with the specified bitmap pattern. The bitmap can be a DIB section bitmap, which is created by the CreateDIBSection function, or it can be a device-dependent bitmap.
helpviewer_keywords: ["CreatePatternBrush","CreatePatternBrush function [Windows GDI]","_win32_CreatePatternBrush","gdi.createpatternbrush","wingdi/CreatePatternBrush"]
old-location: gdi\createpatternbrush.htm
tech.root: gdi
ms.assetid: a3cf347e-9803-4bb0-bdb3-98929ef859ab
ms.date: 12/05/2018
ms.keywords: CreatePatternBrush, CreatePatternBrush function [Windows GDI], _win32_CreatePatternBrush, gdi.createpatternbrush, wingdi/CreatePatternBrush
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
 - CreatePatternBrush
 - wingdi/CreatePatternBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - CreatePatternBrush
---

# CreatePatternBrush function


## -description

The <b>CreatePatternBrush</b> function creates a logical brush with the specified bitmap pattern. The bitmap can be a DIB section bitmap, which is created by the <b>CreateDIBSection</b> function, or it can be a device-dependent bitmap.

## -parameters

### -param hbm [in]

A handle to the bitmap to be used to create the logical brush.

## -returns

If the function succeeds, the return value identifies a logical brush.

If the function fails, the return value is <b>NULL</b>.

## -remarks

A pattern brush is a bitmap that the system uses to paint the interiors of filled shapes.

After an application creates a brush by calling <b>CreatePatternBrush</b>, it can select that brush into any device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function.

You can delete a pattern brush without affecting the associated bitmap by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function. Therefore, you can then use this bitmap to create any number of pattern brushes.

A brush created by using a monochrome (1 bit per pixel) bitmap has the text and background colors of the device context to which it is drawn. Pixels represented by a 0 bit are drawn with the current text color; pixels represented by a 1 bit are drawn with the current background color.

<b>ICM:</b> No color is done at brush creation. However, color management is performed when the brush is selected into an ICM-enabled device context.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-brushes">Using Brushes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/brush-functions">Brush Functions</a>



<a href="/windows/desktop/gdi/brushes">Brushes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmap">CreateBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmapindirect">CreateBitmapIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrushpt">CreateDIBPatternBrushPt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbrushorgex">GetBrushOrgEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadbitmapa">LoadBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbrushorgex">SetBrushOrgEx</a>