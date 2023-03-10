---
UID: NF:wingdi.GetTextExtentPointI
title: GetTextExtentPointI function (wingdi.h)
description: The GetTextExtentPointI function computes the width and height of the specified array of glyph indices.
helpviewer_keywords: ["GetTextExtentPointI","GetTextExtentPointI function [Windows GDI]","_win32_GetTextExtentPointI","gdi.gettextextentpointi","wingdi/GetTextExtentPointI"]
old-location: gdi\gettextextentpointi.htm
tech.root: gdi
ms.assetid: d06a48dd-3f38-4c60-a4c6-954e43f718d1
ms.date: 12/05/2018
ms.keywords: GetTextExtentPointI, GetTextExtentPointI function [Windows GDI], _win32_GetTextExtentPointI, gdi.gettextextentpointi, wingdi/GetTextExtentPointI
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
 - GetTextExtentPointI
 - wingdi/GetTextExtentPointI
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
 - GetTextExtentPointI
---

# GetTextExtentPointI function


## -description

The <b>GetTextExtentPointI</b> function computes the width and height of the specified array of glyph indices.

## -parameters

### -param hdc [in]

Handle to the device context.

### -param pgiIn [in]

Pointer to array of glyph indices.

### -param cgi [in]

Specifies the number of glyph indices.

### -param psize [out]

Pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that receives the dimensions of the string, in logical units.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>GetTextExtentPointI</b> function uses the currently selected font to compute the dimensions of the array of glyph indices. The width and height, in logical units, are computed without considering any clipping.

When this function returns the text extent, it assumes that the text is horizontal, that is, that the escapement is always 0. This is true for both the horizontal and vertical measurements of the text. Even if you use a font that specifies a nonzero escapement, this function doesn't use the angle while it computes the text extent. The app must convert it explicitly. However, when the graphics mode is set to <a href="/windows/desktop/api/wingdi/nf-wingdi-setgraphicsmode">GM_ADVANCED</a> and the character orientation is 90 degrees from the print orientation, the values that this function return do not follow this rule. When the character orientation and the print orientation match for a given string, this function returns the dimensions of the string in the <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure as { cx : 116, cy : 18 }.  When the character orientation and the print orientation are 90 degrees apart for the same string, this function returns the dimensions of the string in the <b>SIZE</b> structure as { cx : 18, cy : 116 }.

Because some devices kern characters, the sum of the extents of the individual glyph indices may not be equal to the extent of the entire array of glyph indices.

The calculated string width takes into account the intercharacter spacing set by the <a href="/windows/desktop/api/wingdi/nf-wingdi-settextcharacterextra">SetTextCharacterExtra</a> function.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa">GetTextExtentPoint</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextcharacterextra">SetTextCharacterExtra</a>