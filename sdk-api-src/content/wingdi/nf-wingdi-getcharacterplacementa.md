---
UID: NF:wingdi.GetCharacterPlacementA
title: GetCharacterPlacementA function (wingdi.h)
description: The GetCharacterPlacement function retrieves information about a character string, such as character widths, caret positioning, ordering within the string, and glyph rendering. (ANSI)
helpviewer_keywords: ["GCP_CLASSIN", "GCP_DIACRITIC", "GCP_DISPLAYZWG", "GCP_GLYPHSHAPE", "GCP_JUSTIFY", "GCP_KASHIDA", "GCP_LIGATE", "GCP_MAXEXTENT", "GCP_NEUTRALOVERRIDE", "GCP_NUMERICOVERRIDE", "GCP_NUMERICSLATIN", "GCP_NUMERICSLOCAL", "GCP_REORDER", "GCP_SYMSWAPOFF", "GCP_USEKERNING", "GetCharacterPlacementA", "wingdi/GetCharacterPlacementA"]
old-location: gdi\getcharacterplacement.htm
tech.root: gdi
ms.assetid: 80d3f4b3-503b-4abb-826c-e5c09972ba2f
ms.date: 12/05/2018
ms.keywords: GCP_CLASSIN, GCP_DIACRITIC, GCP_DISPLAYZWG, GCP_GLYPHSHAPE, GCP_JUSTIFY, GCP_KASHIDA, GCP_LIGATE, GCP_MAXEXTENT, GCP_NEUTRALOVERRIDE, GCP_NUMERICOVERRIDE, GCP_NUMERICSLATIN, GCP_NUMERICSLOCAL, GCP_REORDER, GCP_SYMSWAPOFF, GCP_USEKERNING, GetCharacterPlacement, GetCharacterPlacement function [Windows GDI], GetCharacterPlacementA, GetCharacterPlacementW, _win32_GetCharacterPlacement, gdi.getcharacterplacement, wingdi/GetCharacterPlacement, wingdi/GetCharacterPlacementA, wingdi/GetCharacterPlacementW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCharacterPlacementW (Unicode) and GetCharacterPlacementA (ANSI)
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
 - GetCharacterPlacementA
 - wingdi/GetCharacterPlacementA
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
 - GetCharacterPlacement
 - GetCharacterPlacementA
 - GetCharacterPlacementW
---

# GetCharacterPlacementA function


## -description

The <b>GetCharacterPlacement</b> function retrieves information about a character string, such as character widths, caret positioning, ordering within the string, and glyph rendering. The type of information returned depends on the <i>dwFlags</i> parameter and is based on the currently selected font in the specified display context. The function copies the information to the specified <a href="/windows/desktop/api/wingdi/ns-wingdi-gcp_resultsa">GCP_RESULTS</a> structure or to one or more arrays specified by the structure.

Although this function was once adequate for working with character strings, a need to work with an increasing number of languages and scripts has rendered it obsolete. It has been superseded by the functionality of the Uniscribe module. For more information, see <a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>.

It is recommended that an application use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> function to determine whether the GCP_DIACRITIC, GCP_DBCS, GCP_USEKERNING, GCP_LIGATE, GCP_REORDER, GCP_GLYPHSHAPE, and GCP_KASHIDA values are valid for the currently selected font. If not valid, <b>GetCharacterPlacement</b> ignores the value.

The GCP_NODIACRITICS value is no longer defined and should not be used.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpString [in]

A pointer to the character string to process. The string does not need to be zero-terminated, since <i>nCount</i> specifies the length of the string.

### -param nCount [in]

The <a href="/windows/desktop/gdi/specifying-length-of-text-output-string">length of the string</a> pointed to by <i>lpString</i>.

### -param nMexExtent [in]

The maximum extent (in logical units) to which the string is processed. Characters that, if processed, would exceed this extent are ignored. Computations for any required ordering or glyph arrays apply only to the included characters. This parameter is used only if the GCP_MAXEXTENT value is specified in the <i>dwFlags</i> parameter. As the function processes the input string, each character and its extent is added to the output, extent, and other arrays only if the total extent has not yet exceeded the maximum. Once the limit is reached, processing will stop.

### -param lpResults [in, out]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-gcp_resultsa">GCP_RESULTS</a> structure that receives the results of the function.

### -param dwFlags [in]

Specifies how to process the string into the required arrays. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCP_CLASSIN"></a><a id="gcp_classin"></a><dl>
<dt><b>GCP_CLASSIN</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the <i>lpClass</i> array contains preset classifications for characters. The classifications may be the same as on output. If the particular classification for a character is not known, the corresponding location in the array must be set to zero. for more information about the classifications, see GCP_RESULTS. This is useful only if <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> returned the GCP_REORDER flag.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_DIACRITIC"></a><a id="gcp_diacritic"></a><dl>
<dt><b>GCP_DIACRITIC</b></dt>
</dl>
</td>
<td width="60%">
Determines how diacritics in the string are handled. If this value is not set, diacritics are treated as zero-width characters. For example, a Hebrew string may contain diacritics, but you may not want to display them.

Use <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> to determine whether a font supports diacritics. If it does, you can use or not use the GCP_DIACRITIC flag in the call to <b>GetCharacterPlacement</b>, depending on the needs of your application.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_DISPLAYZWG"></a><a id="gcp_displayzwg"></a><dl>
<dt><b>GCP_DISPLAYZWG</b></dt>
</dl>
</td>
<td width="60%">
For languages that need reordering or different glyph shapes depending on the positions of the characters within a word, nondisplayable characters often appear in the code page. For example, in the Hebrew code page, there are Left-To-Right and Right-To-Left markers, to help determine the final positioning of characters within the output strings. Normally these are not displayed and are removed from the <i>lpGlyphs</i> and <i>lpDx</i> arrays. You can use the GCP_DISPLAYZWG flag to display these characters.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_GLYPHSHAPE"></a><a id="gcp_glyphshape"></a><dl>
<dt><b>GCP_GLYPHSHAPE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that some or all characters in the string are to be displayed using shapes other than the standard shapes defined in the currently selected font for the current code page. Some languages, such as Arabic, cannot support glyph creation unless this value is specified. As a general rule, if <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> returns this value for a string, this value must be used with <b>GetCharacterPlacement</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_JUSTIFY"></a><a id="gcp_justify"></a><dl>
<dt><b>GCP_JUSTIFY</b></dt>
</dl>
</td>
<td width="60%">
Adjusts the extents in the <i>lpDx</i> array so that the string length is the same as <i>nMaxExtent</i>. GCP_JUSTIFY may only be used in conjunction with GCP_MAXEXTENT.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_KASHIDA"></a><a id="gcp_kashida"></a><dl>
<dt><b>GCP_KASHIDA</b></dt>
</dl>
</td>
<td width="60%">
Use Kashidas as well as, or instead of, adjusted extents to modify the length of the string so that it is equal to the value specified by <i>nMaxExtent</i>. In the <i>lpDx</i> array, a Kashida is indicated by a negative justification index. GCP_KASHIDA may be used only in conjunction with GCP_JUSTIFY and only if the font (and language) support Kashidas. Use <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> to determine whether the current font supports Kashidas.

Using Kashidas to justify the string can result in the number of glyphs required being greater than the number of characters in the input string. Because of this, when Kashidas are used, the application cannot assume that setting the arrays to be the size of the input string will be sufficient. (The maximum possible will be approximately dxPageWidth/dxAveCharWidth, where dxPageWidth is the width of the document and dxAveCharWidth is the average character width as returned from a <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics">GetTextMetrics</a> call).

Note that just because <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> returns the GCP_KASHIDA flag does not mean that it has to be used in the call to <b>GetCharacterPlacement</b>, just that the option is available.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_LIGATE"></a><a id="gcp_ligate"></a><dl>
<dt><b>GCP_LIGATE</b></dt>
</dl>
</td>
<td width="60%">
Use ligations wherever characters ligate. A ligation occurs where one glyph is used for two or more characters. For example, the letters a and e can ligate to ?. For this to be used, however, both the language support and the font must support the required glyphs (the example will not be processed by default in English).

Use <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> to determine whether the current font supports ligation. If it does and a specific maximum is required for the number of characters that will ligate, set the number in the first element of the <b>lpGlyphs</b> array. If normal ligation is required, set this value to zero. If GCP_LIGATE is not specified, no ligation will take place. See GCP_RESULTS for more information.

If the GCP_REORDER value is usually required for the character set but is not specified, the output will be meaningless unless the string being passed in is already in visual ordering (that is, the result that gets put into lpGcpResults-&gt;lpOutString in one call to <b>GetCharacterPlacement</b> is the input string of a second call).

Note that just because <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> returns the GCP_LIGATE flag does not mean that it has to be used in the call to <b>GetCharacterPlacement</b>, just that the option is available.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_MAXEXTENT"></a><a id="gcp_maxextent"></a><dl>
<dt><b>GCP_MAXEXTENT</b></dt>
</dl>
</td>
<td width="60%">
Compute extents of the string only as long as the resulting extent, in logical units, does not exceed the values specified by the <i>nMaxExtent</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_NEUTRALOVERRIDE"></a><a id="gcp_neutraloverride"></a><dl>
<dt><b>GCP_NEUTRALOVERRIDE</b></dt>
</dl>
</td>
<td width="60%">
Certain languages only. Override the normal handling of neutrals and treat them as strong characters that match the strings reading order. Useful only with the GCP_REORDER flag.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_NUMERICOVERRIDE"></a><a id="gcp_numericoverride"></a><dl>
<dt><b>GCP_NUMERICOVERRIDE</b></dt>
</dl>
</td>
<td width="60%">
Certain languages only. Override the normal handling of numerics and treat them as strong characters that match the strings reading order. Useful only with the GCP_REORDER flag.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_NUMERICSLATIN"></a><a id="gcp_numericslatin"></a><dl>
<dt><b>GCP_NUMERICSLATIN</b></dt>
</dl>
</td>
<td width="60%">
Arabic/Thai only. Use standard Latin glyphs for numbers and override the system default. To determine if this option is available in the language of the font, use <a href="/previous-versions/ms960831(v%3dmsdn.10)">GetStringTypeEx</a> to see if the language supports more than one number format.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_NUMERICSLOCAL"></a><a id="gcp_numericslocal"></a><dl>
<dt><b>GCP_NUMERICSLOCAL</b></dt>
</dl>
</td>
<td width="60%">
Arabic/Thai only. Use local glyphs for numeric characters and override the system default. To determine if this option is available in the language of the font, use <a href="/previous-versions/ms960831(v%3dmsdn.10)">GetStringTypeEx</a> to see if the language supports more than one number format.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_REORDER"></a><a id="gcp_reorder"></a><dl>
<dt><b>GCP_REORDER</b></dt>
</dl>
</td>
<td width="60%">
Reorder the string. Use for languages that are not SBCS and left-to-right reading order. If this value is not specified, the string is assumed to be in display order already.

If this flag is set for Semitic languages and the <b>lpClass</b> array is used, the first two elements of the array are used to specify the reading order beyond the bounds of the string. GCP_CLASS_PREBOUNDRTL and GCP_CLASS_PREBOUNDLTR can be used to set the order. If no preset order is required, set the values to zero. These values can be combined with other values if the GCPCLASSIN flag is set.

If the GCP_REORDER value is not specified, the <i>lpString</i> parameter is taken to be visual ordered for languages where this is used, and the <i>lpOutString</i> and <i>lpOrder</i> fields are ignored.

Use <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> to determine whether the current font supports reordering.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_SYMSWAPOFF"></a><a id="gcp_symswapoff"></a><dl>
<dt><b>GCP_SYMSWAPOFF</b></dt>
</dl>
</td>
<td width="60%">
Semitic languages only. Specifies that swappable characters are not reset. For example, in a right-to-left string, the '(' and ')' are not reversed.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_USEKERNING"></a><a id="gcp_usekerning"></a><dl>
<dt><b>GCP_USEKERNING</b></dt>
</dl>
</td>
<td width="60%">
Use kerning pairs in the font (if any) when creating the widths arrays. Use <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> to determine whether the current font supports kerning pairs.

Note that just because <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> returns the GCP_USEKERNING flag does not mean that it has to be used in the call to <b>GetCharacterPlacement</b>, just that the option is available. Most TrueType fonts have a kerning table, but you do not have to use it.

</td>
</tr>
</table>
 

It is recommended that an application use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a> function to determine whether the GCP_DIACRITIC, GCP_DBCS, GCP_USEKERNING, GCP_LIGATE, GCP_REORDER, GCP_GLYPHSHAPE, and GCP_KASHIDA values are valid for the currently selected font. If not valid, <b>GetCharacterPlacement</b> ignores the value.

The GCP_NODIACRITICS value is no longer defined and should not be used.

## -returns

If the function succeeds, the return value is the  width and height of the string in logical units. The width is the low-order word and the height is the high-order word.

If the function fails, the return value is zero.

## -remarks

<b>GetCharacterPlacement</b> ensures that an application can correctly process text regardless of the international setting and type of fonts available. Applications use this function before using the <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> function and in place of the <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a> function (and occasionally in place of the <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidth32a">GetCharWidth32</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a> functions).

Using <b>GetCharacterPlacement</b> to retrieve intercharacter spacing and index arrays is not always necessary unless justification or kerning is required. For non-Latin fonts, applications can improve the speed at which the <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> function renders text by using <b>GetCharacterPlacement</b> to retrieve the intercharacter spacing and index arrays before calling <b>ExtTextOut</b>. This is especially useful when rendering the same text repeatedly or when using intercharacter spacing to position the caret. If the <b>lpGlyphs</b> output array is used in the call to <b>ExtTextOut</b>, the ETO_GLYPH_INDEX flag must be set.

<b>GetCharacterPlacement</b> checks the <b>lpOrder</b>, <b>lpDX</b>, <b>lpCaretPos</b>, <b>lpOutString</b>, and <b>lpGlyphs</b> members of the <a href="/windows/desktop/api/wingdi/ns-wingdi-gcp_resultsa">GCP_RESULTS</a> structure and fills the corresponding arrays if these members are not set to <b>NULL</b>. If <b>GetCharacterPlacement</b> cannot fill an array, it sets the corresponding member to <b>NULL</b>. To ensure retrieval of valid information, the application is responsible for setting the member to a valid address before calling the function and for checking the value of the member after the call. If the GCP_JUSTIFY or GCP_USEKERNING values are specified, the <b>lpDX</b> and/or <b>lpCaretPos</b> members must have valid addresses.

Note that the glyph indexes returned in GCP_RESULTS.lpGlyphs are specific to the current font in the device context and should only be used to draw text in the device context while that font remains selected.

When computing justification, if the trailing characters in the string are spaces, the function reduces the length of the string and removes the spaces prior to computing the justification. If the array consists of only spaces, the function returns an error.


<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> expects an <b>lpDX</b> entry for each byte of a DBCS string, whereas <b>GetCharacterPlacement</b> assigns an <b>lpDX</b> entry for each glyph. To correct this mismatch when using this combination of functions, either use <a href="/windows/desktop/api/wingdi/nf-wingdi-getglyphindicesa">GetGlyphIndices</a> or expand the <b>lpDX</b> array with zero-width entries for the corresponding second byte of a DBCS byte pair.

If the logical width is less than the width of the leading character in the input string, GCP_RESULTS.nMaxFit returns a bad value. For this case, call <b>GetCharacterPlacement</b> for glyph indexes and the <b>lpDX</b> array. Then use the <b>lpDX</b> array to do the extent calculation using the advance width of each character, where <b>nMaxFit</b> is the number of characters whose glyph indexes advance width is less than the width of the leading character.





> [!NOTE]
> The wingdi.h header defines GetCharacterPlacement as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-gcp_resultsa">GCP_RESULTS</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcharwidth32a">GetCharWidth32</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getfontlanguageinfo">GetFontLanguageInfo</a>



<a href="/previous-versions/ms960831(v%3dmsdn.10)">GetStringTypeEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics">GetTextMetrics</a>
