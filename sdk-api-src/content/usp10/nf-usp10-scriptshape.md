---
UID: NF:usp10.ScriptShape
title: ScriptShape function (usp10.h)
description: Generates glyphs and visual attributes for a Unicode run.
helpviewer_keywords: ["ScriptShape","ScriptShape function [Internationalization for Windows Applications]","_win32_ScriptShape","intl.scriptshape","usp10/ScriptShape"]
old-location: intl\scriptshape.htm
tech.root: Intl
ms.assetid: 073ba94a-ebfa-42f5-9d90-d5693dc25703
ms.date: 12/05/2018
ms.keywords: ScriptShape, ScriptShape function [Internationalization for Windows Applications], _win32_ScriptShape, intl.scriptshape, usp10/ScriptShape
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ScriptShape
 - usp10/ScriptShape
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
 - ScriptShape
---

# ScriptShape function


## -description

Generates glyphs and visual attributes for a Unicode run.

## -parameters

### -param hdc [in]

Optional. Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param pwcChars [in]

Pointer to an array of Unicode characters defining the run.

### -param cChars [in]

Number of characters in the Unicode run.

### -param cMaxGlyphs [in]

Maximum number of glyphs to generate, and the length of <i>pwOutGlyphs</i>. A reasonable value is <code>(1.5 * cChars + 16)</code>, but this value might be insufficient in some circumstances. For more information, see the Remarks section.

### -param psa [in, out]

Pointer to the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure for the run, containing the results from an earlier call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>.

### -param pwOutGlyphs [out]

Pointer to a buffer in which this function retrieves an array of glyphs with size as indicated by <i>cMaxGlyphs</i>.

### -param pwLogClust [out]

Pointer to a buffer in which this function retrieves an array of logical cluster information. Each array element corresponds to a character in the array of Unicode characters; therefore this array has the number of elements indicated by cChars. The value of each element is the offset from the first glyph in the run to the first glyph in the cluster containing the corresponding character. Note that, when the <b>fRTL</b> member is set to <b>TRUE</b> in the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure, the elements decrease as the array is read.

### -param psva [out]

Pointer to a buffer in which this function retrieves an array of <a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a> structures containing visual attribute information. Since each glyph has only one visual attribute, this array has the number of elements indicated by <i>cMaxGlyphs</i>.

### -param pcGlyphs [out]

Pointer to the location in which this function retrieves the number of glyphs indicated in <i>pwOutGlyphs</i>.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. In all error cases, the content of all output parameters is undefined.

Error returns include:

<ul>
<li>E_OUTOFMEMORY. The output buffer length indicated by <i>cMaxGlyphs</i> is insufficient.</li>
<li>E_PENDING. The script cache specified by the <i>psc</i> parameter does not contain enough information to shape the string, and the device context has been passed as <b>NULL</b> so that the function is unable to complete the shaping process. The application should set up a correct device context for the run, and call this function again with the appropriate value in <i>hdc</i> and with all other parameters the same.</li>
<li>USP_E_SCRIPT_NOT_IN_FONT. The font corresponding to the device context does not support the script required by the run indicated by <i>pwcChars</i>. The application should choose another font, using either <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetcmap">ScriptGetCMap</a> or another function to select the font.</li>
</ul>

## -remarks

See <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

If this function returns E_OUTOFMEMORY, the application might call <b>ScriptShape</b> repeatedly, with successively larger output buffers, until a large enough buffer is provided. The number of glyphs generated by a code point varies according to the script and the font. For a simple script, a Unicode code point might generate a single glyph. However, a complex script font might construct characters from components, and thus generate several times as many glyphs as characters. Also, there are special cases, such as invalid character representations, in which extra glyphs are added to represent the invalid sequence. Therefore, a reasonable guess for the size of the buffer indicated by <i>pwOutGlyphs</i> is 1.5 times the length of the character buffer, plus an additional 16 glyphs for rare cases, for example, invalid sequence representation.

This function can set the <b>fNoGlyphIndex</b> member of the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure if the font or operating system cannot support glyph indexes.

The application can call <b>ScriptShape</b> to determine if a font supports the characters in a given string. If the function returns S_OK, the application should check the output for missing glyphs. If <b>fLogicalOrder</b> is set to <b>TRUE</b> in the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure, the function always generates glyphs in the same order as the original Unicode characters. If <b>fLogicalOrder</b> is set to <b>FALSE</b>, the function generates right-to-left items in reverse order so that <a href="/windows/desktop/api/usp10/nf-usp10-scripttextout">ScriptTextOut</a> does not have to reverse them before calling <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>.

If the <b>eScript</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> is set to SCRIPT_UNDEFINED, shaping is disabled. In this case, <b>ScriptShape</b> displays the glyph that is in the font cmap table. If no glyph is in the table, the function indicates that glyphs are missing.

<b>ScriptShape</b> sequences clusters uniformly within the run, and sequences glyphs uniformly within a cluster. It uses the value of the <b>fRTL</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>, from <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>, to identify sequencing as left-to-right or right-to-left.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

#### Examples

The following example shows how <b>ScriptShape</b> generates a logical cluster array (<i>pwLogClust</i>) from a character array (<i>pwcChars</i>) and a glyph array (<i>pwOutGlyphs</i>). The run has four clusters.

<ul>
<li>First cluster: one character represented by one glyph</li>
<li>Second cluster: one character represented by three glyphs</li>
<li>Third cluster: three characters represented by one glyph</li>
<li>Fourth cluster: two characters represented by three glyphs</li>
</ul>
Character array, where c&lt;n&gt;u&lt;m&gt; means cluster n, Unicode code point m:

<ul>
<li>| c1u1 | c2u1 | c3u1 c3u2 c3u3 | c4u1 c4u2 |</li>
</ul>
Glyph array, where c&lt;n&gt;g&lt;m&gt; means cluster n, glyph m:

<ul>
<li>| c1g1 | c2g1 c2g2 c2g3 | c3g1 | c4g1 c4g2 c4g3 |</li>
</ul>
Cluster array, that is, the offset (in glyphs) to the cluster containing the character:

<ul>
<li>| 0 | 1 | 4 4 4 | 5 5 |</li>
</ul>
<div class="code"></div>

## -see-also

<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshapeopentype">ScriptShapeOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scripttextout">ScriptTextOut</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>