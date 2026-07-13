---
UID: NF:wingdi.GetCharWidthA
title: GetCharWidthA function (wingdi.h)
description: The GetCharWidth function retrieves the widths, in logical coordinates, of consecutive characters in a specified range from the current font. (ANSI)
helpviewer_keywords: ["GetCharWidthA", "wingdi/GetCharWidthA"]
old-location: gdi\getcharwidth.htm
tech.root: gdi
ms.assetid: be29c195-cf67-45d5-8a46-ac572afb756d
ms.date: 12/05/2018
ms.keywords: GetCharWidth, GetCharWidth function [Windows GDI], GetCharWidthA, GetCharWidthW, _win32_GetCharWidth, gdi.getcharwidth, wingdi/GetCharWidth, wingdi/GetCharWidthA, wingdi/GetCharWidthW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCharWidthW (Unicode) and GetCharWidthA (ANSI)
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
 - GetCharWidthA
 - wingdi/GetCharWidthA
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
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetCharWidth
 - GetCharWidthA
 - GetCharWidthW
---

# GetCharWidthA function


## -description

The <b>GetCharWidth</b> function retrieves the widths, in logical coordinates, of consecutive characters in a specified range from the current font.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should call the <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidth32a">GetCharWidth32</a> function, which provides more accurate results.</div><div> </div>

## -parameters

### -param hdc [in]

A handle to the device context.

### -param iFirst [in]

The first character in the group of consecutive characters.

### -param iLast [in]

The last character in the group of consecutive characters, which must not precede the specified first character.

### -param lpBuffer [out]

A pointer to a buffer that receives the character widths, in logical coordinates.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

<b>GetCharWidth</b> cannot be used on TrueType fonts. To retrieve character widths for TrueType fonts, use <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a>.

The range is inclusive; that is, the returned widths include the widths of the characters specified by the <i>iFirstChar</i> and <i>iLastChar</i> parameters.

If a character does not exist in the current font, it is assigned the width of the default character.





> [!NOTE]
> The wingdi.h header defines GetCharWidth as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsfloata">GetCharABCWidthsFloat</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidth32a">GetCharWidth32</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidthfloata">GetCharWidthFloat</a>
