---
UID: NS:wingdi.tagGCP_RESULTSA
title: GCP_RESULTSA (wingdi.h)
description: The GCP_RESULTS structure contains information about characters in a string. This structure receives the results of the GetCharacterPlacement function. For some languages, the first element in the arrays may contain more, language-dependent information. (ANSI)
helpviewer_keywords: ["*LPGCP_RESULTSA","GCPCLASS_ARABIC","GCPCLASS_HEBREW","GCPCLASS_LATIN","GCPCLASS_LATINNUMBER","GCPCLASS_LATINNUMERICSEPARATOR","GCPCLASS_LATINNUMERICTERMINATOR","GCPCLASS_LOCALNUMBER","GCPCLASS_NEUTRAL","GCPCLASS_NUMERICSEPARATOR","GCPCLASS_POSTBOUNDLTR","GCPCLASS_POSTBOUNDRTL","GCPCLASS_PREBOUNDLTR","GCPCLASS_PREBOUNDRTL","GCP_RESULTS","GCP_RESULTS structure [Windows GDI]","GCP_RESULTSA","GCP_RESULTSW","LPGCP_RESULTS","LPGCP_RESULTS structure pointer [Windows GDI]","_win32_GCP_RESULTS_str","gdi.gcp_results","wingdi/GCP_RESULTS","wingdi/GCP_RESULTSA","wingdi/GCP_RESULTSW","wingdi/LPGCP_RESULTS"]
old-location: gdi\gcp_results.htm
tech.root: gdi
ms.assetid: 7692637e-963a-4e0a-8a04-e05a6d01c417
ms.date: 12/05/2018
ms.keywords: '*LPGCP_RESULTSA, GCPCLASS_ARABIC, GCPCLASS_HEBREW, GCPCLASS_LATIN, GCPCLASS_LATINNUMBER, GCPCLASS_LATINNUMERICSEPARATOR, GCPCLASS_LATINNUMERICTERMINATOR, GCPCLASS_LOCALNUMBER, GCPCLASS_NEUTRAL, GCPCLASS_NUMERICSEPARATOR, GCPCLASS_POSTBOUNDLTR, GCPCLASS_POSTBOUNDRTL, GCPCLASS_PREBOUNDLTR, GCPCLASS_PREBOUNDRTL, GCP_RESULTS, GCP_RESULTS structure [Windows GDI], GCP_RESULTSA, GCP_RESULTSW, LPGCP_RESULTS, LPGCP_RESULTS structure pointer [Windows GDI], _win32_GCP_RESULTS_str, gdi.gcp_results, wingdi/GCP_RESULTS, wingdi/GCP_RESULTSA, wingdi/GCP_RESULTSW, wingdi/LPGCP_RESULTS'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GCP_RESULTSW (Unicode) and GCP_RESULTSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GCP_RESULTSA, *LPGCP_RESULTSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagGCP_RESULTSA
 - wingdi/tagGCP_RESULTSA
 - LPGCP_RESULTSA
 - wingdi/LPGCP_RESULTSA
 - GCP_RESULTSA
 - wingdi/GCP_RESULTSA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - GCP_RESULTS
 - GCP_RESULTSA
 - GCP_RESULTSW
---

# GCP_RESULTSA structure


## -description

The <b>GCP_RESULTS</b> structure contains information about characters in a string. This structure receives the results of the <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> function. For some languages, the first element in the arrays may contain more, language-dependent information.

## -struct-fields

### -field lStructSize

The size, in bytes, of the structure.

### -field lpOutString

A pointer to the buffer that receives the output string or is <b>NULL</b> if the output string is not needed. The output string is a version of the original string that is in the order that will be displayed on a specified device. Typically the output string is identical to the original string, but may be different if the string needs reordering and the GCP_REORDER flag is set or if the original string exceeds the maximum extent and the GCP_MAXEXTENT flag is set.

### -field lpOrder

A pointer to the array that receives ordering indexes or is <b>NULL</b> if the ordering indexes are not needed. However, its meaning depends on the other elements of <b>GCP_RESULTS</b>. If glyph indexes are to be returned, the indexes are for the <b>lpGlyphs</b> array; if glyphs indexes are not returned and <b>lpOrder</b> is requested, the indexes are for <b>lpOutString</b>. For example, in the latter case the value of <b>lpOrder</b>[i] is the position of <b>lpString</b>[i] in the output string lpOutString.

This is typically used when <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> returns the GCP_REORDER flag, which indicates that the original string needs reordering. For example, in Hebrew, in which the text runs from right to left, the <b>lpOrder</b> array gives the exact locations of each element in the original string.

### -field lpDx

A pointer to the array that receives the distances between adjacent character cells or is <b>NULL</b> if these distances are not needed. If glyph rendering is done, the distances are for the glyphs not the characters, so the resulting array can be used with the <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> function.

The distances in this array are in display order. To find the distance for the <i>i</i><sup>th</sup> character in the original string, use the <b>lpOrder</b> array as follows:


``` syntax

width = lpDx[lpOrder[i]];

```


### -field lpCaretPos

A pointer to the array that receives the caret position values or is <b>NULL</b> if caret positions are not needed. Each value specifies the caret position immediately before the corresponding character. In some languages the position of the caret for each character may not be immediately to the left of the character. For example, in Hebrew, in which the text runs from right to left, the caret position is to the right of the character. If glyph ordering is done, <b>lpCaretPos</b> matches the original string, not the output string. This means that some adjacent values may be the same.

The values in this array are in input order. To find the caret position value for the <i>i</i><sup>th</sup> character in the original string, use the array as follows:


``` syntax

position = lpCaretPos[i];

```


### -field lpClass

A pointer to the array that contains and/or receives character classifications. The values indicate how to lay out characters in the string and are similar (but not identical) to the CT_CTYPE2 values returned by the <a href="/previous-versions/ms960831(v%3dmsdn.10)">GetStringTypeEx</a> function. Each element of the array can be set to zero or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_ARABIC"></a><a id="gcpclass_arabic"></a><dl>
<dt><b>GCPCLASS_ARABIC</b></dt>
</dl>
</td>
<td width="60%">
Arabic character.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_HEBREW"></a><a id="gcpclass_hebrew"></a><dl>
<dt><b>GCPCLASS_HEBREW</b></dt>
</dl>
</td>
<td width="60%">
Hebrew character.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_LATIN"></a><a id="gcpclass_latin"></a><dl>
<dt><b>GCPCLASS_LATIN</b></dt>
</dl>
</td>
<td width="60%">
Character from a Latin or other single-byte character set for a left-to-right language.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_LATINNUMBER"></a><a id="gcpclass_latinnumber"></a><dl>
<dt><b>GCPCLASS_LATINNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Digit from a Latin or other single-byte character set for a left-to-right language.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_LOCALNUMBER"></a><a id="gcpclass_localnumber"></a><dl>
<dt><b>GCPCLASS_LOCALNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Digit from the character set associated with the current font.

</td>
</tr>
</table>
 

In addition, the following can be used when supplying values in the <b>lpClass</b> array with the GCP_CLASSIN flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_LATINNUMERICSEPARATOR"></a><a id="gcpclass_latinnumericseparator"></a><dl>
<dt><b>GCPCLASS_LATINNUMERICSEPARATOR</b></dt>
</dl>
</td>
<td width="60%">
Input only. Character used to separate Latin digits, such as a comma or decimal point.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_LATINNUMERICTERMINATOR"></a><a id="gcpclass_latinnumericterminator"></a><dl>
<dt><b>GCPCLASS_LATINNUMERICTERMINATOR</b></dt>
</dl>
</td>
<td width="60%">
Input only. Character used to terminate Latin digits, such as a plus or minus sign.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_NEUTRAL"></a><a id="gcpclass_neutral"></a><dl>
<dt><b>GCPCLASS_NEUTRAL</b></dt>
</dl>
</td>
<td width="60%">
Input only. Character has no specific classification.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_NUMERICSEPARATOR"></a><a id="gcpclass_numericseparator"></a><dl>
<dt><b>GCPCLASS_NUMERICSEPARATOR</b></dt>
</dl>
</td>
<td width="60%">
Input only. Character used to separate digits, such as a comma or decimal point.

</td>
</tr>
</table>
 

For languages that use the GCP_REORDER flag, the following values can also be used with the GCP_CLASSIN flag. Unlike the preceding values, which can be used anywhere in the <b>lpClass</b> array, all of the following values are used only in the first location in the array. All combine with other classifications.

Note that GCPCLASS_PREBOUNDLTR and GCPCLASS_PREBOUNDRTL are mutually exclusive, as are GCPCLASSPOSTBOUNDLTR and GCPCLASSPOSTBOUNDRTL.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_PREBOUNDLTR"></a><a id="gcpclass_preboundltr"></a><dl>
<dt><b>GCPCLASS_PREBOUNDLTR</b></dt>
</dl>
</td>
<td width="60%">
Set <b>lpClass</b>[0] to GCPCLASS_PREBOUNDLTR to bind the string to left-to-right reading order before the string.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_PREBOUNDRTL"></a><a id="gcpclass_preboundrtl"></a><dl>
<dt><b>GCPCLASS_PREBOUNDRTL</b></dt>
</dl>
</td>
<td width="60%">
Set <b>lpClass</b>[0] to GCPCLASS_PREBOUNDRTL to bind the string to right-to-left reading order before the string.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_POSTBOUNDLTR"></a><a id="gcpclass_postboundltr"></a><dl>
<dt><b>GCPCLASS_POSTBOUNDLTR</b></dt>
</dl>
</td>
<td width="60%">
Set <b>lpClass</b>[0] to GCPCLASS_POSTBOUNDLTR to bind the string to left-to-right reading order after the string.

</td>
</tr>
<tr>
<td width="40%"><a id="GCPCLASS_POSTBOUNDRTL"></a><a id="gcpclass_postboundrtl"></a><dl>
<dt><b>GCPCLASS_POSTBOUNDRTL</b></dt>
</dl>
</td>
<td width="60%">
Set <b>lpClass</b>[0] to GCPCLASS_POSTBOUNDRTL to bind the string to right-to-left reading order after the string.

</td>
</tr>
</table>
 

To force the layout of a character to be carried out in a specific way, preset the classification for the corresponding array element; the function leaves such preset classifications unchanged and computes classifications only for array elements that have been set to zero. Preset classifications are used only if the GCP_CLASSIN flag is set and the <b>lpClass</b> array is supplied.

If <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> does not return GCP_REORDER for the current font, only the GCPCLASS_LATIN value is meaningful.

### -field lpGlyphs

A pointer to the array that receives the values identifying the glyphs used for rendering the string or is <b>NULL</b> if glyph rendering is not needed. The number of glyphs in the array may be less than the number of characters in the original string if the string contains ligated glyphs. Also if reordering is required, the order of the glyphs may not be sequential.

This array is useful if more than one operation is being done on a string which has any form of ligation, kerning or order-switching. Using the values in this array for subsequent operations saves the time otherwise required to generate the glyph indices each time.

This array always contains glyph indices and the ETO_GLYPH_INDEX value must always be used when this array is used with the <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> function.

When GCP_LIGATE is used, you can limit the number of characters that will be ligated together. (In Arabic for example, three-character ligations are common). This is done by setting the maximum required in lpGcpResults-&gt;lpGlyphs[0]. If no maximum is required, you should set this field to zero.

For languages such as Arabic, where <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> returns the GCP_GLYPHSHAPE flag, the glyphs for a character will be different depending on whether the character is at the beginning, middle, or end of a word. Typically, the first character in the input string will also be the first character in a word, and the last character in the input string will be treated as the last character in a word. However, if the displayed string is a subset of the complete string, such as when displaying a section of scrolled text, this may not be true. In these cases, it is desirable to force the first or last characters to be shaped as not being initial or final forms. To do this, again, the first location in the <b>lpGlyphs</b> array is used by performing an OR operation of the ligation value above with the values GCPGLYPH_LINKBEFORE and/or GCPGLYPH_LINKAFTER. For example, a value of GCPGLYPH_LINKBEFORE | 2 means that two-character ligatures are the maximum required, and the first character in the string should be treated as if it is in the middle of a word.

### -field nGlyphs

On input, this member must be set to the size of the arrays pointed to by the array pointer members. On output, this is set to the number of glyphs filled in, in the output arrays. If glyph substitution is not required (that is, each input character maps to exactly one glyph), this member is the same as it is on input.

### -field nMaxFit

The number of characters that fit within the extents specified by the <i>nMaxExtent</i> parameter of the <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> function. If the GCP_MAXEXTENT or GCP_JUSTIFY value is set, this value may be less than the number of characters in the original string. This member is set regardless of whether the GCP_MAXEXTENT or GCP_JUSTIFY value is specified. Unlike <b>nGlyphs</b>, which specifies the number of output glyphs, <b>nMaxFit</b> refers to the number of characters from the input string. For Latin SBCS languages, this will be the same.

## -remarks

Whether the <b>lpGlyphs</b>, <b>lpOutString</b>, or neither is required depends on the results of the <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> call.

In the case of a font for a language such as English, in which none of the GCP_DBCS, GCP_REORDER, GCP_GLYPHSHAPE, GCP_LIGATE, GCP_DIACRITIC, or GCP_KASHIDA flags are returned, neither of the arrays is required for proper operation. (Though not required, they can still be used. If the <b>lpOutString</b> array is used, it will be exactly the same as the <i>lpInputString</i> passed to <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>.) Note, however, that if GCP_MAXEXTENT is used, then <b>lpOutString</b> will contain the truncated string if it is used, NOT an exact copy of the original.

In the case of fonts for languages such as Hebrew, which DO have reordering but do not typically have extra glyph shapes, <b>lpOutString</b> should be used. This will give the string on the screen-readable order. However, the <b>lpGlyphs</b> array is not typically needed. (Hebrew can have extra glyphs, if the font is a TrueType/Open font.)

In the case of languages such as Thai or Arabic, in which <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> returns the GCP_GLYPHSHAPE flag, the <b>lpOutString</b> will give the display-readable order of the string passed to <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, but the values will still be the unshaped characters. For proper display, the <b>lpGlyphs</b> array must be used.





> [!NOTE]
> The wingdi.h header defines GCP_RESULTS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a>
