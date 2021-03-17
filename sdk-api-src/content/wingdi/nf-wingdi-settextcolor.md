---
UID: NF:wingdi.SetTextColor
title: SetTextColor function (wingdi.h)
description: The SetTextColor function sets the text color for the specified device context to the specified color.
helpviewer_keywords: ["SetTextColor","SetTextColor function [Windows GDI]","_win32_SetTextColor","gdi.settextcolor","wingdi/SetTextColor"]
old-location: gdi\settextcolor.htm
tech.root: gdi
ms.assetid: 3875a247-7c32-4917-bf6d-50b2a49848a6
ms.date: 12/05/2018
ms.keywords: SetTextColor, SetTextColor function [Windows GDI], _win32_SetTextColor, gdi.settextcolor, wingdi/SetTextColor
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
 - SetTextColor
 - wingdi/SetTextColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-0.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetTextColor
---

# SetTextColor function


## -description

The <b>SetTextColor</b> function sets the text color for the specified device context to the specified color.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param color [in]

The color of the text.

## -returns

If the function succeeds, the return value is a color reference for the previous text color as a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value.

If the function fails, the return value is CLR_INVALID.

## -remarks

The text color is used to draw the face of each character written by the <a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> functions. The text color is also used in converting bitmaps from color to monochrome and vice versa.


#### Examples

For an example, see "Setting Fonts for Menu-Item Text Strings" in <a href="/windows/desktop/menurc/using-menus">Using Menus</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextcolor">GetTextColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor">SetBkColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>