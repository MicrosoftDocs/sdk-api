---
UID: NF:wingdi.GetCharWidth32A
title: GetCharWidth32A function (wingdi.h)
description: The GetCharWidth32 function retrieves the widths, in logical coordinates, of consecutive characters in a specified range from the current font. (ANSI)
helpviewer_keywords: ["GetCharWidth32A", "wingdi/GetCharWidth32A"]
old-location: gdi\getcharwidth32.htm
tech.root: gdi
ms.assetid: f7d6e9b3-72aa-42d8-8346-b230b9e98237
ms.date: 12/05/2018
ms.keywords: GetCharWidth32, GetCharWidth32 function [Windows GDI], GetCharWidth32A, GetCharWidth32W, _win32_GetCharWidth32, gdi.getcharwidth32, wingdi/GetCharWidth32, wingdi/GetCharWidth32A, wingdi/GetCharWidth32W
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCharWidth32W (Unicode) and GetCharWidth32A (ANSI)
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
 - GetCharWidth32A
 - wingdi/GetCharWidth32A
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetCharWidth32
 - GetCharWidth32A
 - GetCharWidth32W
---

# GetCharWidth32A function


## -description

The <b>GetCharWidth32</b> function retrieves the widths, in logical coordinates, of consecutive characters in a specified range from the current font.

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

<b>GetCharWidth32</b> cannot be used on TrueType fonts. To retrieve character widths for TrueType fonts, use <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a>.

The range is inclusive; that is, the returned widths include the widths of the characters specified by the <i>iFirstChar</i> and <i>iLastChar</i> parameters.

If a character does not exist in the current font, it is assigned the width of the default character.


#### Examples

For an example, see "Displaying Keyboard Input" in <a href="/windows/desktop/inputdev/using-keyboard-input">Using Keyboard Input</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines GetCharWidth32 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsfloata">GetCharABCWidthsFloat</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidthfloata">GetCharWidthFloat</a>
