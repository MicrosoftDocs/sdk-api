---
UID: NF:wingdi.SetBkColor
title: SetBkColor function (wingdi.h)
description: The SetBkColor function sets the current background color to the specified color value, or to the nearest physical color if the device cannot represent the specified color value.
helpviewer_keywords: ["SetBkColor","SetBkColor function [Windows GDI]","_win32_SetBkColor","gdi.setbkcolor","wingdi/SetBkColor"]
old-location: gdi\setbkcolor.htm
tech.root: gdi
ms.assetid: 9163370b-19c5-4c23-9197-793e4b8d50c4
ms.date: 12/05/2018
ms.keywords: SetBkColor, SetBkColor function [Windows GDI], _win32_SetBkColor, gdi.setbkcolor, wingdi/SetBkColor
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
 - SetBkColor
 - wingdi/SetBkColor
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
 - Ext-MS-Win-GDI-Draw-L1-1-0.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetBkColor
---

# SetBkColor function


## -description

The <b>SetBkColor</b> function sets the current background color to the specified color value, or to the nearest physical color if the device cannot represent the specified color value.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param color [in]

The new background color. To make a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -returns

If the function succeeds, the return value specifies the previous background color as a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value.

If the function fails, the return value is CLR_INVALID.

## -remarks

This function fills the gaps between styled lines drawn using a pen created by the <a href="/windows/desktop/api/wingdi/nf-wingdi-createpen">CreatePen</a> function; it does not fill the gaps between styled lines drawn using a pen created by the <a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a> function. The <b>SetBkColor</b> function also sets the background colors for <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>.

If the background mode is OPAQUE, the background color is used to fill gaps between styled lines, gaps between hatched lines in brushes, and character cells. The background color is also used when converting bitmaps from color to monochrome and vice versa.


#### Examples

For an example, see "Example of Owner-Drawn Menu Items" in <a href="/windows/desktop/menurc/using-menus">Using Menus</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpen">CreatePen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbkcolor">GetBKColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbkmode">GetBkMode</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbkmode">SetBkMode</a>