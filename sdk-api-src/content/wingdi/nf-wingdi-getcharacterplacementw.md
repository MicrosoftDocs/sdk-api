---
UID: NF:wingdi.GetCharacterPlacementW
title: GetCharacterPlacementW function
author: windows-sdk-content
description: The GetCharacterPlacement function retrieves information about a character string, such as character widths, caret positioning, ordering within the string, and glyph rendering.
old-location: gdi\getcharacterplacement.htm
old-project: gdi
ms.assetid: 80d3f4b3-503b-4abb-826c-e5c09972ba2f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GCP_CLASSIN, GCP_DIACRITIC, GCP_DISPLAYZWG, GCP_GLYPHSHAPE, GCP_JUSTIFY, GCP_KASHIDA, GCP_LIGATE, GCP_MAXEXTENT, GCP_NEUTRALOVERRIDE, GCP_NUMERICOVERRIDE, GCP_NUMERICSLATIN, GCP_NUMERICSLOCAL, GCP_REORDER, GCP_SYMSWAPOFF, GCP_USEKERNING, GetCharacterPlacement, GetCharacterPlacement function [Windows GDI], GetCharacterPlacementA, GetCharacterPlacementW, _win32_GetCharacterPlacement, gdi.getcharacterplacement, wingdi/GetCharacterPlacement, wingdi/GetCharacterPlacementA, wingdi/GetCharacterPlacementW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	GetCharacterPlacement
-	GetCharacterPlacementA
-	GetCharacterPlacementW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCharacterPlacementW function


## -description


The <b>GetCharacterPlacement</b> function retrieves information about a character string, such as character widths, caret positioning, ordering within the string, and glyph rendering. The type of information returned depends on the <i>dwFlags</i> parameter and is based on the currently selected font in the specified display context. The function copies the information to the specified <a href="https://msdn.microsoft.com/7692637e-963a-4e0a-8a04-e05a6d01c417">GCP_RESULTS</a> structure or to one or more arrays specified by the structure.

Although this function was once adequate for working with character strings, a need to work with an increasing number of languages and scripts has rendered it obsolete. It has been superseded by the functionality of the Uniscribe module. For more information, see <a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>.

It is recommended that an application use the <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> function to determine whether the GCP_DIACRITIC, GCP_DBCS, GCP_USEKERNING, GCP_LIGATE, GCP_REORDER, GCP_GLYPHSHAPE, and GCP_KASHIDA values are valid for the currently selected font. If not valid, <b>GetCharacterPlacement</b> ignores the value.

The GCP_NODIACRITICS value is no longer defined and should not be used.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpString [in]

A pointer to the character string to process. The string does not need to be zero-terminated, since <i>nCount</i> specifies the length of the string.


### -param nCount [in]

The <a href="https://msdn.microsoft.com/695fd0f9-abd4-4666-acad-2c409624ddc6">length of the string</a> pointed to by <i>lpString</i>.


### -param nMexExtent

TBD


### -param lpResults [in, out]

A pointer to a <a href="https://msdn.microsoft.com/7692637e-963a-4e0a-8a04-e05a6d01c417">GCP_RESULTS</a> structure that receives the results of the function.


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
Specifies that the <i>lpClass</i> array contains preset classifications for characters. The classifications may be the same as on output. If the particular classification for a character is not known, the corresponding location in the array must be set to zero. for more information about the classifications, see GCP_RESULTS. This is useful only if <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> returned the GCP_REORDER flag.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_DIACRITIC"></a><a id="gcp_diacritic"></a><dl>
<dt><b>GCP_DIACRITIC</b></dt>
</dl>
</td>
<td width="60%">
Determines how diacritics in the string are handled. If this value is not set, diacritics are treated as zero-width characters. For example, a Hebrew string may contain diacritics, but you may not want to display them.

Use <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> to determine whether a font supports diacritics. If it does, you can use or not use the GCP_DIACRITIC flag in the call to <b>GetCharacterPlacement</b>, depending on the needs of your application.

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
Specifies that some or all characters in the string are to be displayed using shapes other than the standard shapes defined in the currently selected font for the current code page. Some languages, such as Arabic, cannot support glyph creation unless this value is specified. As a general rule, if <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> returns this value for a string, this value must be used with <b>GetCharacterPlacement</b>.

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
Use Kashidas as well as, or instead of, adjusted extents to modify the length of the string so that it is equal to the value specified by <i>nMaxExtent</i>. In the <i>lpDx</i> array, a Kashida is indicated by a negative justification index. GCP_KASHIDA may be used only in conjunction with GCP_JUSTIFY and only if the font (and language) support Kashidas. Use <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> to determine whether the current font supports Kashidas.

Using Kashidas to justify the string can result in the number of glyphs required being greater than the number of characters in the input string. Because of this, when Kashidas are used, the application cannot assume that setting the arrays to be the size of the input string will be sufficient. (The maximum possible will be approximately dxPageWidth/dxAveCharWidth, where dxPageWidth is the width of the document and dxAveCharWidth is the average character width as returned from a <a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a> call).

Note that just because <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> returns the GCP_KASHIDA flag does not mean that it has to be used in the call to <b>GetCharacterPlacement</b>, just that the option is available.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_LIGATE"></a><a id="gcp_ligate"></a><dl>
<dt><b>GCP_LIGATE</b></dt>
</dl>
</td>
<td width="60%">
Use ligations wherever characters ligate. A ligation occurs where one glyph is used for two or more characters. For example, the letters a and e can ligate to ?. For this to be used, however, both the language support and the font must support the required glyphs (the example will not be processed by default in English).

Use <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> to determine whether the current font supports ligation. If it does and a specific maximum is required for the number of characters that will ligate, set the number in the first element of the <b>lpGlyphs</b> array. If normal ligation is required, set this value to zero. If GCP_LIGATE is not specified, no ligation will take place. See GCP_RESULTS for more information.

If the GCP_REORDER value is usually required for the character set but is not specified, the output will be meaningless unless the string being passed in is already in visual ordering (that is, the result that gets put into lpGcpResults-&gt;lpOutString in one call to <b>GetCharacterPlacement</b> is the input string of a second call).

Note that just because <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> returns the GCP_LIGATE flag does not mean that it has to be used in the call to <b>GetCharacterPlacement</b>, just that the option is available.

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
Arabic/Thai only. Use standard Latin glyphs for numbers and override the system default. To determine if this option is available in the language of the font, use <a href="_win32_getstringtypeex_cpp">GetStringTypeEx</a> to see if the language supports more than one number format.

</td>
</tr>
<tr>
<td width="40%"><a id="GCP_NUMERICSLOCAL"></a><a id="gcp_numericslocal"></a><dl>
<dt><b>GCP_NUMERICSLOCAL</b></dt>
</dl>
</td>
<td width="60%">
Arabic/Thai only. Use local glyphs for numeric characters and override the system default. To determine if this option is available in the language of the font, use <a href="_win32_getstringtypeex_cpp">GetStringTypeEx</a> to see if the language supports more than one number format.

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

Use <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> to determine whether the current font supports reordering.

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
Use kerning pairs in the font (if any) when creating the widths arrays. Use <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> to determine whether the current font supports kerning pairs.

Note that just because <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> returns the GCP_USEKERNING flag does not mean that it has to be used in the call to <b>GetCharacterPlacement</b>, just that the option is available. Most TrueType fonts have a kerning table, but you do not have to use it.

</td>
</tr>
</table>
 

It is recommended that an application use the <a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a> function to determine whether the GCP_DIACRITIC, GCP_DBCS, GCP_USEKERNING, GCP_LIGATE, GCP_REORDER, GCP_GLYPHSHAPE, and GCP_KASHIDA values are valid for the currently selected font. If not valid, <b>GetCharacterPlacement</b> ignores the value.

The GCP_NODIACRITICS value is no longer defined and should not be used.


#### - nMaxExtent [in]

The maximum extent (in logical units) to which the string is processed. Characters that, if processed, would exceed this extent are ignored. Computations for any required ordering or glyph arrays apply only to the included characters. This parameter is used only if the GCP_MAXEXTENT value is specified in the <i>dwFlags</i> parameter. As the function processes the input string, each character and its extent is added to the output, extent, and other arrays only if the total extent has not yet exceeded the maximum. Once the limit is reached, processing will stop.


## -returns



If the function succeeds, the return value is the  width and height of the string in logical units. The width is the low-order word and the height is the high-order word.

If the function fails, the return value is zero.




## -remarks



<b>GetCharacterPlacement</b> ensures that an application can correctly process text regardless of the international setting and type of fonts available. Applications use this function before using the <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> function and in place of the <a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a> function (and occasionally in place of the <a href="https://msdn.microsoft.com/f7d6e9b3-72aa-42d8-8346-b230b9e98237">GetCharWidth32</a> and <a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a> functions).

Using <b>GetCharacterPlacement</b> to retrieve intercharacter spacing and index arrays is not always necessary unless justification or kerning is required. For non-Latin fonts, applications can improve the speed at which the <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> function renders text by using <b>GetCharacterPlacement</b> to retrieve the intercharacter spacing and index arrays before calling <b>ExtTextOut</b>. This is especially useful when rendering the same text repeatedly or when using intercharacter spacing to position the caret. If the <b>lpGlyphs</b> output array is used in the call to <b>ExtTextOut</b>, the ETO_GLYPH_INDEX flag must be set.

<b>GetCharacterPlacement</b> checks the <b>lpOrder</b>, <b>lpDX</b>, <b>lpCaretPos</b>, <b>lpOutString</b>, and <b>lpGlyphs</b> members of the <a href="https://msdn.microsoft.com/7692637e-963a-4e0a-8a04-e05a6d01c417">GCP_RESULTS</a> structure and fills the corresponding arrays if these members are not set to <b>NULL</b>. If <b>GetCharacterPlacement</b> cannot fill an array, it sets the corresponding member to <b>NULL</b>. To ensure retrieval of valid information, the application is responsible for setting the member to a valid address before calling the function and for checking the value of the member after the call. If the GCP_JUSTIFY or GCP_USEKERNING values are specified, the <b>lpDX</b> and/or <b>lpCaretPos</b> members must have valid addresses.

Note that the glyph indexes returned in GCP_RESULTS.lpGlyphs are specific to the current font in the device context and should only be used to draw text in the device context while that font remains selected.

When computing justification, if the trailing characters in the string are spaces, the function reduces the length of the string and removes the spaces prior to computing the justification. If the array consists of only spaces, the function returns an error.


<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> expects an <b>lpDX</b> entry for each byte of a DBCS string, whereas <b>GetCharacterPlacement</b> assigns an <b>lpDX</b> entry for each glyph. To correct this mismatch when using this combination of functions, either use <a href="https://msdn.microsoft.com/7abfee7a-dd5d-4f33-96f1-b38364ba5afd">GetGlyphIndices</a> or expand the <b>lpDX</b> array with zero-width entries for the corresponding second byte of a DBCS byte pair.


         If the logical width is less than the width of the leading character in the input string, GCP_RESULTS.nMaxFit returns a bad value. For this case, call <b>GetCharacterPlacement</b> for glyph indexes and the <b>lpDX</b> array. Then use the <b>lpDX</b> array to do the extent calculation using the advance width of each character, where <b>nMaxFit</b> is the number of characters whose glyph indexes advance width is less than the width of the leading character.




## -see-also




<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/7692637e-963a-4e0a-8a04-e05a6d01c417">GCP_RESULTS</a>



<a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a>



<a href="https://msdn.microsoft.com/f7d6e9b3-72aa-42d8-8346-b230b9e98237">GetCharWidth32</a>



<a href="https://msdn.microsoft.com/c2f19423-4410-44dd-83f1-5b858852051d">GetFontLanguageInfo</a>



<a href="_win32_getstringtypeex_cpp">GetStringTypeEx</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a>
 

 

