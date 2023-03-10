---
UID: NF:wingdi.GetCharABCWidthsI
title: GetCharABCWidthsI function (wingdi.h)
description: The GetCharABCWidthsI function retrieves the widths, in logical units, of consecutive glyph indices in a specified range from the current TrueType font. This function succeeds only with TrueType fonts.
helpviewer_keywords: ["GetCharABCWidthsI","GetCharABCWidthsI function [Windows GDI]","_win32_GetCharABCWidthsI","gdi.getcharabcwidthsi","wingdi/GetCharABCWidthsI"]
old-location: gdi\getcharabcwidthsi.htm
tech.root: gdi
ms.assetid: 7d1210ee-42b7-4f2e-9e89-fb1543d76290
ms.date: 12/05/2018
ms.keywords: GetCharABCWidthsI, GetCharABCWidthsI function [Windows GDI], _win32_GetCharABCWidthsI, gdi.getcharabcwidthsi, wingdi/GetCharABCWidthsI
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
 - GetCharABCWidthsI
 - wingdi/GetCharABCWidthsI
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
 - GetCharABCWidthsI
---

# GetCharABCWidthsI function


## -description

The <b>GetCharABCWidthsI</b> function retrieves the widths, in logical units, of consecutive glyph indices in a specified range from the current TrueType font. This function succeeds only with TrueType fonts.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param giFirst [in]

The first glyph index in the group of consecutive glyph indices from the current font. This parameter is only used if the <i>pgi</i> parameter is <b>NULL</b>.

### -param cgi [in]

The number of glyph indices.

### -param pgi [in]

A pointer to an array that contains glyph indices. If this parameter is <b>NULL</b>, the <i>giFirst</i> parameter is used instead. The <i>cgi</i> parameter specifies the number of glyph indices in this array.

### -param pabc [out]

A pointer to an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-abc">ABC</a> structures that receives the character widths, in logical units. This array must contain at least as many <b>ABC</b> structures as there are glyph indices specified by the <i>cgi</i> parameter.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The TrueType rasterizer provides ABC character spacing after a specific point size has been selected. A spacing is the distance added to the current position before placing the glyph. B spacing is the width of the black part of the glyph. C spacing is the distance added to the current position to provide white space to the right of the glyph. The total advanced width is specified by A+B+C.

When the <b>GetCharABCWidthsI</b> function retrieves negative A or C widths for a character, that character includes underhangs or overhangs.

To convert the ABC widths to font design units, an application should use the value stored in the <b>otmEMSquare</b> member of a <a href="/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a> structure. This value can be retrieved by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getoutlinetextmetricsa">GetOutlineTextMetrics</a> function.

The ABC widths of the default character are used for characters outside the range of the currently selected font.

To retrieve the widths of glyph indices in non-TrueType fonts, applications should use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidthi">GetCharWidthI</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-abc">ABC</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidtha">GetCharWidth</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getoutlinetextmetricsa">GetOutlineTextMetrics</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a>