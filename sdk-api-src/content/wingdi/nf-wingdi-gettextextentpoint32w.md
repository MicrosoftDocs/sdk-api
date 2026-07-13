---
UID: NF:wingdi.GetTextExtentPoint32W
title: GetTextExtentPoint32W function (wingdi.h)
description: The GetTextExtentPoint32 function computes the width and height of the specified string of text. (Unicode)
helpviewer_keywords: ["GetTextExtentPoint32", "GetTextExtentPoint32 function [Windows GDI]", "GetTextExtentPoint32W", "_win32_GetTextExtentPoint32", "gdi.gettextextentpoint32", "wingdi/GetTextExtentPoint32", "wingdi/GetTextExtentPoint32W"]
old-location: gdi\gettextextentpoint32.htm
tech.root: gdi
ms.assetid: 530280ee-dfd8-4905-9b72-6c19efcff133
ms.date: 12/05/2018
ms.keywords: GetTextExtentPoint32, GetTextExtentPoint32 function [Windows GDI], GetTextExtentPoint32A, GetTextExtentPoint32W, _win32_GetTextExtentPoint32, gdi.gettextextentpoint32, wingdi/GetTextExtentPoint32, wingdi/GetTextExtentPoint32A, wingdi/GetTextExtentPoint32W
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTextExtentPoint32W (Unicode) and GetTextExtentPoint32A (ANSI)
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
 - GetTextExtentPoint32W
 - wingdi/GetTextExtentPoint32W
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
 - GetTextExtentPoint32
 - GetTextExtentPoint32A
 - GetTextExtentPoint32W
---

# GetTextExtentPoint32W function


## -description

The <b>GetTextExtentPoint32</b> function computes the width and height of the specified string of text.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpString [in]

A pointer to a buffer that specifies the text string. The string does not need to be null-terminated, because the <i>c</i> parameter specifies the length of the string.

### -param c [in]

The <a href="/windows/desktop/gdi/specifying-length-of-text-output-string">length of the string</a> pointed to by <i>lpString</i>.

### -param psizl [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that receives the dimensions of the string, in logical units.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>GetTextExtentPoint32</b> function uses the currently selected font to compute the dimensions of the string. The width and height, in logical units, are computed without considering any clipping.

Because some devices kern characters, the sum of the extents of the characters in a string may not be equal to the extent of the string.

The calculated string width takes into account the intercharacter spacing set by the <a href="/windows/desktop/api/wingdi/nf-wingdi-settextcharacterextra">SetTextCharacterExtra</a> function and the justification set by <a href="/windows/desktop/api/wingdi/nf-wingdi-settextjustification">SetTextJustification</a>. This is true for both displaying on a screen and for printing. However, if <i>lpDx</i> is set in <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>, <b>GetTextExtentPoint32</b> does not take into account either intercharacter spacing or justification. In addition, for EMF, the print result always takes both intercharacter spacing and justification into account.

When dealing with text displayed on a screen, the calculated string width takes into account the intercharacter spacing set by the <a href="/windows/desktop/api/wingdi/nf-wingdi-settextcharacterextra">SetTextCharacterExtra</a> function and the justification set by <a href="/windows/desktop/api/wingdi/nf-wingdi-settextjustification">SetTextJustification</a>. However, if <i>lpDx</i> is set in <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>, <b>GetTextExtentPoint32</b> does not take into account either intercharacter spacing or justification. However, when printing with EMF:

<ul>
<li>The print result ignores intercharacter spacing, although <b>GetTextExtentPoint32</b> takes it into account.</li>
<li>The print result takes justification into account, although <b>GetTextExtentPoint32</b> ignores it.</li>
</ul>
When this function returns the text extent, it assumes that the text is horizontal, that is, that the escapement is always 0. This is true for both the horizontal and vertical measurements of the text. Even if you use a font that specifies a nonzero escapement, this function doesn't use the angle while it computes the text extent. The app must convert it explicitly. However, when the graphics mode is set to <a href="/windows/desktop/api/wingdi/nf-wingdi-setgraphicsmode">GM_ADVANCED</a> and the character orientation is 90 degrees from the print orientation, the values that this function return do not follow this rule. When the character orientation and the print orientation match for a given string, this function returns the dimensions of the string in the <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure as { cx : 116, cy : 18 }.  When the character orientation and the print orientation are 90 degrees apart for the same string, this function returns the dimensions of the string in the <b>SIZE</b> structure as { cx : 18, cy : 116 }.

<b>GetTextExtentPoint32</b> doesn't consider "\n" (new line) or "\r\n" (carriage return and new line) characters when it computes the height of a text string.


#### Examples

For an example, see <a href="/windows/desktop/gdi/drawing-text-from-different-fonts-on-the-same-line">Drawing Text from Different Fonts on the Same Line</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines GetTextExtentPoint32 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextcharacterextra">SetTextCharacterExtra</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextjustification">SetTextJustification</a>
