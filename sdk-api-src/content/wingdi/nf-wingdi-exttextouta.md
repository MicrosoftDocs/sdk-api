---
UID: NF:wingdi.ExtTextOutA
title: ExtTextOutA function (wingdi.h)
description: The ExtTextOut function draws text using the currently selected font, background color, and text color. You can optionally provide dimensions to be used for clipping, opaquing, or both. (ANSI)
helpviewer_keywords: ["ETO_CLIPPED", "ETO_GLYPH_INDEX", "ETO_IGNORELANGUAGE", "ETO_NUMERICSLATIN", "ETO_NUMERICSLOCAL", "ETO_OPAQUE", "ETO_PDY", "ETO_RTLREADING", "ExtTextOutA", "wingdi/ExtTextOutA"]
old-location: gdi\exttextout.htm
tech.root: gdi
ms.assetid: 74f8fcb8-8ad4-47f2-a330-fa56713bdb37
ms.date: 12/05/2018
ms.keywords: ETO_CLIPPED, ETO_GLYPH_INDEX, ETO_IGNORELANGUAGE, ETO_NUMERICSLATIN, ETO_NUMERICSLOCAL, ETO_OPAQUE, ETO_PDY, ETO_RTLREADING, ExtTextOut, ExtTextOut function [Windows GDI], ExtTextOutA, ExtTextOutW, _win32_ExtTextOut, gdi.exttextout, wingdi/ExtTextOut, wingdi/ExtTextOutA, wingdi/ExtTextOutW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExtTextOutW (Unicode) and ExtTextOutA (ANSI)
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
 - ExtTextOutA
 - wingdi/ExtTextOutA
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
 - ExtTextOut
 - ExtTextOutA
 - ExtTextOutW
---

# ExtTextOutA function


## -description

The <b>ExtTextOut</b> function draws text using the currently selected font, background color, and text color. You can optionally provide dimensions to be used for clipping, opaquing, or both.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The x-coordinate, in logical coordinates, of the reference point used to position the string.

### -param y [in]

The y-coordinate, in logical coordinates, of the reference point used to position the string.

### -param options [in]

Specifies how to use the application-defined rectangle. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ETO_CLIPPED"></a><a id="eto_clipped"></a><dl>
<dt><b>ETO_CLIPPED</b></dt>
</dl>
</td>
<td width="60%">
The text will be clipped to the rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="ETO_GLYPH_INDEX"></a><a id="eto_glyph_index"></a><dl>
<dt><b>ETO_GLYPH_INDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpString</i> array refers to an array returned from <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> and should be parsed directly by GDI as no further language-specific processing is required. Glyph indexing only applies to TrueType fonts, but the flag can be used for bitmap and vector fonts to indicate that no further language processing is necessary and GDI should process the string directly. Note that all glyph indexes are 16-bit values even though the string is assumed to be an array of 8-bit values for raster fonts.

For ExtTextOutW, the glyph indexes are saved to a metafile. However, to display the correct characters the metafile must be played back using the same font. For ExtTextOutA, the glyph indexes are not saved.

</td>
</tr>
<tr>
<td width="40%"><a id="ETO_IGNORELANGUAGE"></a><a id="eto_ignorelanguage"></a><dl>
<dt><b>ETO_IGNORELANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for system use. If an application sets this flag, it loses international scripting support and in some cases it may display no text at all.

</td>
</tr>
<tr>
<td width="40%"><a id="ETO_NUMERICSLATIN"></a><a id="eto_numericslatin"></a><dl>
<dt><b>ETO_NUMERICSLATIN</b></dt>
</dl>
</td>
<td width="60%">
To display numbers, use European digits.

</td>
</tr>
<tr>
<td width="40%"><a id="ETO_NUMERICSLOCAL"></a><a id="eto_numericslocal"></a><dl>
<dt><b>ETO_NUMERICSLOCAL</b></dt>
</dl>
</td>
<td width="60%">
To display numbers, use digits appropriate to the locale.

</td>
</tr>
<tr>
<td width="40%"><a id="ETO_OPAQUE"></a><a id="eto_opaque"></a><dl>
<dt><b>ETO_OPAQUE</b></dt>
</dl>
</td>
<td width="60%">
The current background color should be used to fill the rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="ETO_PDY"></a><a id="eto_pdy"></a><dl>
<dt><b>ETO_PDY</b></dt>
</dl>
</td>
<td width="60%">
When this is set, the array pointed to by <i>lpDx</i> contains pairs of values. The first value of each pair is, as usual, the distance between origins of adjacent character cells, but the second value is the displacement along the vertical direction of the font.

</td>
</tr>
<tr>
<td width="40%"><a id="ETO_RTLREADING"></a><a id="eto_rtlreading"></a><dl>
<dt><b>ETO_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
<b>Middle East language edition of Windows:</b> If this value is specified and a Hebrew or Arabic font is selected into the device context, the string is output using right-to-left reading order. If this value is not specified, the string is output in left-to-right order. The same effect can be achieved by setting the TA_RTLREADING value in <a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a>. This value is preserved for backward compatibility.

</td>
</tr>
</table>
 

The ETO_GLYPH_INDEX and ETO_RTLREADING values cannot be used together. Because ETO_GLYPH_INDEX implies that all language processing has been completed, the function ignores the ETO_RTLREADING flag if also specified.

### -param lprect [in]

A pointer to an optional <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the dimensions, in logical coordinates, of a rectangle that is used for clipping, opaquing, or both.

### -param lpString [in]

A pointer to a string that specifies the text to be drawn. The string does not need to be zero-terminated, since <i>cbCount</i> specifies the length of the string.

### -param c [in]

The <a href="/windows/desktop/gdi/specifying-length-of-text-output-string">length of the string</a> pointed to by <i>lpString</i>.

This value may not exceed 8192.

### -param lpDx [in]

A pointer to an optional array of values that indicate the distance between origins of adjacent character cells. For example, lpDx[<i>i</i>] logical units separate the origins of character cell <i>i</i> and character cell <i>i</i> + 1.

## -returns

If the string is drawn, the return value is nonzero. However, if the ANSI version of <b>ExtTextOut</b> is called with ETO_GLYPH_INDEX, the function returns <b>TRUE</b> even though the function does nothing.

If the function fails, the return value is zero.

## -remarks

The current text-alignment settings for the specified device context determine how the reference point is used to position the text. The text-alignment settings are retrieved by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextalign">GetTextAlign</a> function. The text-alignment settings are altered by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a> function. You can use the following values for text alignment. Only one flag can be chosen from those that affect horizontal and vertical alignment. In addition, only one of the two flags that alter the current position can be chosen.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="TA_BASELINE"></a><a id="ta_baseline"></a>TA_BASELINE

</td>
<td width="60%">
The reference point will be on the base line of the text.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_BOTTOM"></a><a id="ta_bottom"></a>TA_BOTTOM

</td>
<td width="60%">
The reference point will be on the bottom edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_TOP"></a><a id="ta_top"></a>TA_TOP

</td>
<td width="60%">
The reference point will be on the top edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_CENTER"></a><a id="ta_center"></a>TA_CENTER

</td>
<td width="60%">
The reference point will be aligned horizontally with the center of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_LEFT"></a><a id="ta_left"></a>TA_LEFT

</td>
<td width="60%">
The reference point will be on the left edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_RIGHT"></a><a id="ta_right"></a>TA_RIGHT

</td>
<td width="60%">
The reference point will be on the right edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_NOUPDATECP"></a><a id="ta_noupdatecp"></a>TA_NOUPDATECP

</td>
<td width="60%">
The current position is not updated after each text output call. The reference point is passed to the text output function.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_RTLREADING"></a><a id="ta_rtlreading"></a>TA_RTLREADING

</td>
<td width="60%">
<b>Middle East language edition of Windows:</b> The text is laid out in right to left reading order, as opposed to the default left to right order. This applies only when the font selected into the device context is either Hebrew or Arabic.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_UPDATECP"></a><a id="ta_updatecp"></a>TA_UPDATECP

</td>
<td width="60%">
The current position is updated after each text output call. The current position is used as the reference point.

</td>
</tr>
</table>
 

If the <i>lpDx</i> parameter is <b>NULL</b>, the <b>ExtTextOut</b> function uses the default spacing between characters. The character-cell origins and the contents of the array pointed to by the <i>lpDx</i> parameter are specified in logical units. A character-cell origin is defined as the upper-left corner of the character cell.

By default, the current position is not used or updated by this function. However, an application can call the <a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a> function with the <i>fMode</i> parameter set to TA_UPDATECP to permit the system to use and update the current position each time the application calls <b>ExtTextOut</b> for a specified device context. When this flag is set, the system ignores the <i>X</i> and <i>Y</i> parameters on subsequent <b>ExtTextOut</b> calls.

For the ANSI version of <b>ExtTextOut</b>, the <i>lpDx</i> array has the same number of INT values as there are bytes in <i>lpString</i>. For DBCS characters, you can apportion the dx in the <i>lpDx</i> entries between the lead byte and the trail byte, as long as the sum of the two bytes adds up to the desired dx. For DBCS characters with the Unicode version of <b>ExtTextOut</b>, each Unicode glyph gets a single <i>pdx</i> entry.

Note, the <i>alpDx</i> values from <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentexpointa">GetTextExtentExPoint</a> are not the same as the <i>lpDx</i> values for <b>ExtTextOut</b>. To use the <i>alpDx</i> values in <i>lpDx</i>, you must first process them.


**ExtTextOut** will use [Uniscribe](/windows/win32/intl/uniscribe) when necessary resulting in font fallback. The ETO_IGNORELANGUAGE flag will inhibit this behavior and should not be passed.

Additionally, **ExtTextOut** will perform internal batching of calls before transitioning to kernel mode, mitigating some of the performance concerns when weighing usage of **PolyTextOut** versus **ExtTextOut**.

> [!TIP]
>  **ExtTextOut** is strongly recommended over **PolyTextOut** for modern development due to its ability to handle display of different languages.

#### Examples

For an example, see "Setting Fonts for Menu-Item Text Strings" in <a href="/windows/desktop/menurc/using-menus">Using Menus</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines ExtTextOut as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextalign">GetTextAlign</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor">SetBkColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextcolor">SetTextColor</a>
