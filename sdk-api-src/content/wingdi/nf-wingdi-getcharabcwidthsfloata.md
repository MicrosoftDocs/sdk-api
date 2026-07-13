---
UID: NF:wingdi.GetCharABCWidthsFloatA
title: GetCharABCWidthsFloatA function (wingdi.h)
description: The GetCharABCWidthsFloat function retrieves the widths, in logical units, of consecutive characters in a specified range from the current font. (ANSI)
helpviewer_keywords: ["GetCharABCWidthsFloatA", "wingdi/GetCharABCWidthsFloatA"]
old-location: gdi\getcharabcwidthsfloat.htm
tech.root: gdi
ms.assetid: 552942c9-e2a6-43f9-901f-3aba1e2523e5
ms.date: 12/05/2018
ms.keywords: GetCharABCWidthsFloat, GetCharABCWidthsFloat function [Windows GDI], GetCharABCWidthsFloatA, GetCharABCWidthsFloatW, _win32_GetCharABCWidthsFloat, gdi.getcharabcwidthsfloat, wingdi/GetCharABCWidthsFloat, wingdi/GetCharABCWidthsFloatA, wingdi/GetCharABCWidthsFloatW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCharABCWidthsFloatW (Unicode) and GetCharABCWidthsFloatA (ANSI)
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
 - GetCharABCWidthsFloatA
 - wingdi/GetCharABCWidthsFloatA
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
 - GetCharABCWidthsFloat
 - GetCharABCWidthsFloatA
 - GetCharABCWidthsFloatW
---

# GetCharABCWidthsFloatA function


## -description

The <b>GetCharABCWidthsFloat</b> function retrieves the widths, in logical units, of consecutive characters in a specified range from the current font.

## -parameters

### -param hdc [in]

Handle to the device context.

### -param iFirst [in]

Specifies the code point of the first character in the group of consecutive characters where the ABC widths are seeked.

### -param iLast [in]

Specifies the code point of the last character in the group of consecutive characters where the ABC widths are seeked. This range is inclusive. An error is returned if the specified last character precedes the specified first character.

### -param lpABC [out]

Pointer to an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-abcfloat">ABCFLOAT</a> structures that receives the character widths, in logical units.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Unlike the <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a> function that returns widths only for TrueType fonts, the <b>GetCharABCWidthsFloat</b> function retrieves widths for any font. The widths returned by this function are in the IEEE floating-point format.

If the current world-to-device transformation is not identified, the returned widths may be noninteger values, even if the corresponding values in the device space are integers.

A spacing is the distance added to the current position before placing the glyph. B spacing is the width of the black part of the glyph. C spacing is the distance added to the current position to provide white space to the right of the glyph. The total advanced width is specified by A+B+C.

The ABC spaces are measured along the character base line of the selected font.

The ABC widths of the default character are used for characters outside the range of the currently selected font.





> [!NOTE]
> The wingdi.h header defines GetCharABCWidthsFloat as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-abcfloat">ABCFLOAT</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidtha">GetCharWidth</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidthfloata">GetCharWidthFloat</a>
