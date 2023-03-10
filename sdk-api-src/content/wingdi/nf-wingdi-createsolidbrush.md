---
UID: NF:wingdi.CreateSolidBrush
title: CreateSolidBrush function (wingdi.h)
description: The CreateSolidBrush function creates a logical brush that has the specified solid color.
helpviewer_keywords: ["CreateSolidBrush","CreateSolidBrush function [Windows GDI]","_win32_CreateSolidBrush","gdi.createsolidbrush","wingdi/CreateSolidBrush"]
old-location: gdi\createsolidbrush.htm
tech.root: gdi
ms.assetid: e39b5f77-97d8-4ea6-8277-7da12b3367f3
ms.date: 12/05/2018
ms.keywords: CreateSolidBrush, CreateSolidBrush function [Windows GDI], _win32_CreateSolidBrush, gdi.createsolidbrush, wingdi/CreateSolidBrush
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
 - CreateSolidBrush
 - wingdi/CreateSolidBrush
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
 - CreateSolidBrush
---

# CreateSolidBrush function


## -description

The <b>CreateSolidBrush</b> function creates a logical brush that has the specified solid color.

## -parameters

### -param color [in]

The color of the brush. To create a <a href="/windows/desktop/gdi/colorref">COLORREF</a> color value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -returns

If the function succeeds, the return value identifies a logical brush.

If the function fails, the return value is <b>NULL</b>.

## -remarks

When you no longer need the <b>HBRUSH</b> object, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

A solid brush is a bitmap that the system uses to paint the interiors of filled shapes.

After an application creates a brush by calling <b>CreateSolidBrush</b>, it can select that brush into any device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function.

To paint with a system color brush, an application should use <code>GetSysColorBrush (nIndex)</code> instead of <code>CreateSolidBrush(GetSysColor(nIndex))</code>, because <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush">GetSysColorBrush</a> returns a cached brush instead of allocating a new one.

<b>ICM:</b> No color management is done at brush creation. However, color management is performed when the brush is selected into an ICM-enabled device context.


#### Examples

For an example, see <a href="/windows/desktop/gdi/creating-colored-pens-and-brushes">Creating Colored Pens and Brushes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/brush-functions">Brush Functions</a>



<a href="/windows/desktop/gdi/brushes">Brushes Overview</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrushpt">CreateDIBPatternBrushPt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush">GetSysColorBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>