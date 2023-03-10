---
UID: NF:usp10.ScriptShapeOpenType
title: ScriptShapeOpenType function (usp10.h)
description: Generates glyphs and visual attributes for a Unicode run with OpenType information. Each run consists of one call to this function.
helpviewer_keywords: ["ScriptShapeOpenType","ScriptShapeOpenType function [Internationalization for Windows Applications]","_win32_ScriptShapeOpenType","intl.scriptshapeopentype","usp10/ScriptShapeOpenType"]
old-location: intl\scriptshapeopentype.htm
tech.root: Intl
ms.assetid: d2e062a6-2ec8-4057-b525-d1cd719dc736
ms.date: 12/05/2018
ms.keywords: ScriptShapeOpenType, ScriptShapeOpenType function [Internationalization for Windows Applications], _win32_ScriptShapeOpenType, intl.scriptshapeopentype, usp10/ScriptShapeOpenType
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.redist: Usp10.dll version 1.600 or greater on Windows XP
ms.custom: 19H1
f1_keywords:
 - ScriptShapeOpenType
 - usp10/ScriptShapeOpenType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptShapeOpenType
---

# ScriptShapeOpenType function


## -description

Generates glyphs and visual attributes for a Unicode run with OpenType information. Each run consists of one call to this function.

## -parameters

### -param hdc [in, optional]

Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param psa [in, out]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>. The structure identifies the shaping engine, so that glyphs can be formed correctly.

Alternatively, the application can set this parameter to <b>NULL</b> to receive unfiltered results.

### -param tagScript [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure defining the OpenType script tag for the writing system.

### -param tagLangSys [in]

An <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structure containing the OpenType language tag for the writing system.

### -param rcRangeChars [in, optional]

Array of characters in each <a href="/windows/desktop/Intl/uniscribe-glossary">range</a>. The number of array elements is indicated by <i>cRanges</i>. The values of the elements of this array add up to the value of <i>cChars</i>.

### -param rpRangeProperties [in, optional]

Array of <a href="/windows/desktop/api/usp10/ns-usp10-textrange_properties">TEXTRANGE_PROPERTIES</a> structures, each representing one OpenType feature range. The number of structures is indicated by the <i>cRanges</i> parameter. For more information on <i>rpRangeProperties</i>, see the Remarks section.

### -param cRanges [in]

The number of OpenType feature ranges.

### -param pwcChars [in]

Pointer to an array of Unicode characters containing the run.

### -param cChars [in]

Number of characters in the Unicode run.

### -param cMaxGlyphs [in]

Maximum number of glyphs to generate.

### -param pwLogClust [out]

Pointer to a buffer in which this function retrieves an array of logical <a href="/windows/desktop/Intl/uniscribe-glossary">cluster</a> information. Each array element corresponds to a character in the array of Unicode characters. The value of each element is the offset from the first glyph in the run to the first glyph in the cluster containing the corresponding character. Note that, when the <b>fRTL</b> member of the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure is <b>TRUE</b>, the elements decrease as the array is read.

### -param pCharProps [out]

Pointer to a buffer in which this function retrieves an array of character property values, of length indicated by <i>cChars</i>.

### -param pwOutGlyphs [out]

Pointer to a buffer in which this function retrieves an array of glyphs.

### -param pOutGlyphProps [out]

Pointer to a buffer in which this function retrieves an array of attributes for each of the retrieved glyphs. The length of the values equals the value of <i>pcGlyphs</i>. Since one glyph property is indicated per glyph, the value of this parameter indicates the number of elements specified by <i>cMaxGlyphs</i>.

### -param pcGlyphs [out]

Pointer to the location in which this function retrieves the number of glyphs indicated in <i>pwOutGlyphs</i>.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. In all error cases, the content of all output array values is undefined.

Error returns include:

<ul>
<li>E_OUTOFMEMORY. The output buffer length indicated by <i>cMaxGlyphs</i> is insufficient.</li>
<li>E_PENDING. The script cache specified by the <i>psc</i> parameter does not contain enough information to shape the string, and the device context has been passed as <b>NULL</b> so that the function is unable to complete the shaping process. The application should set up a correct device context for the run and call this function again with the appropriate context value in <i>hdc</i> and with all other parameters the same.</li>
<li>USP_E_SCRIPT_NOT_IN_FONT. The font corresponding to the device context does not support the required script. The application should choose another font, using either <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetcmap">ScriptGetCMap</a> or another method to select the font.</li>
</ul>

## -remarks

<b>ScriptShapeOpenType</b> is preferred over the older <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a> function. Some advantages of the <b>ScriptShapeOpenType</b> include the following:

<ul>
<li>Parameters directly correspond to OpenType tags in font layout tables.</li>
<li>Parameters define features applied to each character.</li>
<li>Input is divided into runs. Each run has OpenType properties and consists of a single call to <b>ScriptShapeOpenType</b>.</li>
</ul>
If this function returns E_OUTOFMEMORY, the application might call <b>ScriptShapeOpenType</b> repeatedly, with successively larger output buffers, until a large enough buffer is provided. The number of glyphs generated by a code point varies according to the script and the font. For a simple script, a Unicode code point might generate a single glyph. However, a complex script font might construct characters from components, and thus generate several times as many glyphs as characters. Also, there are special cases, such as invalid character representations, in which extra glyphs are added to represent the invalid sequence. Therefore, a reasonable guess for the size of the buffer indicated by <i>pwOutGlyphs</i> is 1.5 times the length of the character buffer, plus an additional 16 glyphs for rare cases, for example, invalid sequence representation.

This function can set the <b>fNoGlyphIndex</b> member of the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure if the font or operating system cannot support glyph indexes.

The application can call <b>ScriptShapeOpenType</b> to determine if a font supports the characters in a given string. If the function returns S_OK, the application should check the output for missing glyphs. If <b>fLogicalOrder</b> is set to <b>TRUE</b> in the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure, the function always generates glyphs in the same order as the original Unicode characters. If <b>fLogicalOrder</b> is set to <b>FALSE</b>, the function generates right-to-left items in reverse order so that <a href="/windows/desktop/api/usp10/nf-usp10-scripttextout">ScriptTextOut</a> does not have to reverse them before calling <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>.

If the <b>eScript</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> is set to SCRIPT_UNDEFINED, shaping is disabled. In this case, <b>ScriptShapeOpenType</b> displays the glyph that is in the font cmap table. If no glyph is in the table, the function indicates that glyphs are missing.

<b>ScriptShapeOpenType</b> sequences clusters uniformly within the run, and sequences glyphs uniformly within a cluster. It uses the value of the <b>fRTL</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>, from <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>, to identify if sequencing is left-to-right or right-to-left.

For the <i>rpRangeProperties</i> parameter, the <a href="/windows/desktop/api/usp10/ns-usp10-textrange_properties">TEXTRANGE_PROPERTIES</a> structure points to an array of <a href="/windows/desktop/api/usp10/ns-usp10-opentype_feature_record">OPENTYPE_FEATURE_RECORD</a> structures. This array is used as follows:

<ul>
<li>Each element of the array indicated for <i>rpRangeProperties</i> describes a range.</li>
<li>Spans of text sharing particular properties tend to "nest," and nested spans can share <a href="/windows/desktop/api/usp10/ns-usp10-opentype_feature_record">OPENTYPE_FEATURE_RECORD</a> information. For example, in the illustration below:<ul>
<li>The rows of numbers at the top represent ranges, items, and runs, respectively.</li>
<li>Each span labeled here with a letter represents a single OpenType feature. The features that fall into each range are stored in the <a href="/windows/desktop/api/usp10/ns-usp10-opentype_feature_record">OPENTYPE_FEATURE_RECORD</a> array of that range.</li>
<li>For each range, the array of <a href="/windows/desktop/api/usp10/ns-usp10-opentype_feature_record">OPENTYPE_FEATURE_RECORD</a> structures corresponds to the letters for the spans that contain that range.</li>
<li>In this illustration, range 2 is indirectly associated with the <a href="/windows/desktop/api/usp10/ns-usp10-opentype_feature_record">OPENTYPE_FEATURE_RECORD</a> structures for spans A, B, and C. Range 4 is associated only with the structures for spans A and D.</li>
</ul>
</li>
</ul>
<img alt="Illustration showing the range, item, run, and feature of each word in a line of text that uses six properties to present eight words" border="" src="./images/Nested_Properties.GIF"/>
<div class="alert"><b>Note</b>  The illustration makes use of many calls to <b>ScriptShapeOpenType</b>, each representing one run.</div>
<div> </div>
<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

#### Examples

The following example shows how <b>ScriptShapeOpenType</b> generates a logical cluster array (<i>pwLogClust</i>) from a character array (<i>pwcChars</i>) and a glyph array (<i>pwOutGlyphs</i>). The run has four clusters.

<ul>
<li>First cluster: one character represented by one glyph</li>
<li>Second cluster: one character represented by three glyphs</li>
<li>Third cluster: three characters represented by one glyph</li>
<li>Fourth cluster: two characters represented by three glyphs</li>
</ul>
The run is described as follows in the character and glyph arrays.

Character array:

<ul>
<li>| c1u1 | c2u1 | c3u1 c3u2 c3u3 | c4u1 c4u2 |</li>
</ul>
Glyph array:



<ul>
<li>| c1g1 | c2g1 c2g2 c2g3 | c3g1 | c4g1 c4g2 c4g3 |</li>
</ul>
Notation for the array elements consists of these items: 

<ul>
<li>c&lt;n&gt; means cluster n.</li>
<li>g&lt;m&gt; means glyph m.</li>
<li>u&lt;p&gt; means Unicode code point p.</li>
</ul>
The generated cluster array stores offsets to the cluster containing the character. Units are expressed in glyphs.

<ul>
<li>| 0 | 1 | 4 4 4 | 5 5 |</li>
</ul>
<div class="code"></div>

## -see-also

<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/desktop/api/usp10/ns-usp10-opentype_feature_record">OPENTYPE_FEATURE_RECORD</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplaceopentype">ScriptPlaceOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scripttextout">ScriptTextOut</a>



<a href="/windows/desktop/api/usp10/ns-usp10-textrange_properties">TEXTRANGE_PROPERTIES</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>