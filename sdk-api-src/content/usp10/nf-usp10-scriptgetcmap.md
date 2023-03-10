---
UID: NF:usp10.ScriptGetCMap
title: ScriptGetCMap function (usp10.h)
description: Retrieves the glyph indexes of the Unicode characters in a string according to either the TrueType cmap table or the standard cmap table implemented for old-style fonts.
helpviewer_keywords: ["SGCM_RTL","ScriptGetCMap","ScriptGetCMap function [Internationalization for Windows Applications]","_win32_ScriptGetCMap","intl.scriptgetcmap","usp10/ScriptGetCMap"]
old-location: intl\scriptgetcmap.htm
tech.root: Intl
ms.assetid: 577c356d-a22d-422c-bec7-cfbc228f1066
ms.date: 12/05/2018
ms.keywords: SGCM_RTL, ScriptGetCMap, ScriptGetCMap function [Internationalization for Windows Applications], _win32_ScriptGetCMap, intl.scriptgetcmap, usp10/ScriptGetCMap
req.header: usp10.h
req.include-header: 
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
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
f1_keywords:
 - ScriptGetCMap
 - usp10/ScriptGetCMap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptGetCMap
---

# ScriptGetCMap function


## -description

Retrieves the glyph indexes of the Unicode characters in a string according to either the TrueType cmap table or the standard cmap table implemented for old-style fonts.

## -parameters

### -param hdc [in]

Optional. Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param pwcInChars [in]

Pointer to a string of Unicode characters.

### -param cChars [in]

Number of Unicode characters in the string indicated by <i>pwcInChars</i>.

### -param dwFlags [in]

Flags specifying any special handling of the glyphs. By default, the glyphs are provided in logical order with no special handling. This parameter can have the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SGCM_RTL"></a><a id="sgcm_rtl"></a><dl>
<dt><b>SGCM_RTL</b></dt>
</dl>
</td>
<td width="60%">
The glyph array indicated by <i>pwOutGlyphs</i> should contain mirrored glyphs for those glyphs that have a mirrored equivalent.

</td>
</tr>
</table>

### -param pwOutGlyphs [out]

Pointer to a buffer in which the function retrieves an array of glyph indexes. This buffer should be of the same length as the input buffer indicated by <i>pwcInChars</i>. Each code point maps to a single glyph.

## -returns

Returns S_OK if all Unicode code points are present in the font. The function returns one of the nonzero HRESULT values listed below if it does not succeed.
            

<table>
<tr>
<th>Return value</th>
<th>Meaning</th>
</tr>
<tr>
<td>E_HANDLE</td>
<td>The font or the operating system does not support glyph indexes.</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>Some of the Unicode code points were mapped to the default glyph.</td>
</tr>
</table>

## -remarks

See <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

This function can be used to determine the characters in a run that are supported by the selected font. The application can scan the retrieved glyph buffer, looking for the default glyph to determine characters that are not available. The application should determine the default glyph index for the selected font by calling <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetfontproperties">ScriptGetFontProperties</a>.

The return value for this function indicates the presence of any missing glyphs.

<div class="alert"><b>Note</b>  The function assumes a 1:1 relationship between the elements in the input and output arrays. However, the function does not support this relationship for UTF-16 surrogate pairs. For a surrogate pair, the function does not retrieve the glyph index for the supplementary-plane character. Similarly, the function does not support Unicode Variation-Selector (VS) sequences, each of which consists of a Unicode graphic character followed by one of a set of VARIATION SELECTOR characters to select a particular glyph representation for that graphic character. For a VS sequence, the function retrieves the glyph index for the default glyph mapped by the cmap for the two characters, instead of the glyph index for the particular glyph for the VS sequence.</div>
<div> </div>
Some code points can be rendered by a combination of glyphs, as well as by a single glyph, for example, 00C9; LATIN CAPITAL LETTER E WITH ACUTE. In this case, if the font supports the capital E glyph and the acute glyph, but not a single glyph for 00C9, <b>ScriptGetCMap</b> shows that 00C9 is unsupported. To determine the font support for a string that contains these kinds of code points, the application can call <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>. If the function returns S_OK, the application should check the output for missing glyphs.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptgetfontproperties">ScriptGetFontProperties</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>