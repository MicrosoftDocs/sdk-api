---
UID: NF:wingdi.GetCharABCWidthsA
title: GetCharABCWidthsA function (wingdi.h)
description: The GetCharABCWidths function retrieves the widths, in logical units, of consecutive characters in a specified range from the current TrueType font. This function succeeds only with TrueType fonts.helpviewer_keywords: ["GetCharABCWidths","GetCharABCWidths function [Windows GDI]","GetCharABCWidthsA","GetCharABCWidthsW","_win32_GetCharABCWidths","gdi.getcharabcwidths","wingdi/GetCharABCWidths","wingdi/GetCharABCWidthsA","wingdi/GetCharABCWidthsW"]
old-location: gdi\getcharabcwidths.htm
tech.root: gdi
ms.assetid: b48ab66d-ff0a-48d9-b7dd-28610bf69d51
ms.date: 12/05/2018
ms.keywords: GetCharABCWidths, GetCharABCWidths function [Windows GDI], GetCharABCWidthsA, GetCharABCWidthsW, _win32_GetCharABCWidths, gdi.getcharabcwidths, wingdi/GetCharABCWidths, wingdi/GetCharABCWidthsA, wingdi/GetCharABCWidthsW
f1_keywords:
- wingdi/GetCharABCWidths
dev_langs:
- c++
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCharABCWidthsW (Unicode) and GetCharABCWidthsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- gdi32.dll
- Ext-MS-Win-GDI-Font-l1-1-1.dll
- ext-ms-win-gdi-font-l1-1-2.dll
- Ext-MS-Win-GDI-Font-L1-1-3.dll
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32Full.dll
api_name:
- GetCharABCWidths
- GetCharABCWidthsA
- GetCharABCWidthsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCharABCWidthsA function


## -description


The <b>GetCharABCWidths</b> function retrieves the widths, in logical units, of consecutive characters in a specified range from the current TrueType font. This function succeeds only with TrueType fonts.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param wFirst [in]

The first character in the group of consecutive characters from the current font.


### -param wLast [in]

The last character in the group of consecutive characters from the current font.


### -param lpABC [out]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-abc">ABC</a> structures that receives the character widths, in logical units. This array must contain at least as many <b>ABC</b> structures as there are characters in the range specified by the <i>uFirstChar</i> and <i>uLastChar</i> parameters.


## -returns



If the function succeeds, the return value is nonzero

If the function fails, the return value is zero.




## -remarks



The TrueType rasterizer provides ABC character spacing after a specific point size has been selected. A spacing is the distance added to the current position before placing the glyph. B spacing is the width of the black part of the glyph. C spacing is the distance added to the current position to provide white space to the right of the glyph. The total advanced width is specified by A+B+C.

When the <b>GetCharABCWidths</b> function retrieves negative A or C widths for a character, that character includes underhangs or overhangs.

To convert the ABC widths to font design units, an application should use the value stored in the <b>otmEMSquare</b> member of a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a> structure. This value can be retrieved by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getoutlinetextmetricsa">GetOutlineTextMetrics</a> function.

The ABC widths of the default character are used for characters outside the range of the currently selected font.

To retrieve the widths of characters in non-TrueType fonts, applications should use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getcharwidtha">GetCharWidth</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-abc">ABC</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getcharwidtha">GetCharWidth</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getoutlinetextmetricsa">GetOutlineTextMetrics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a>
 

 

