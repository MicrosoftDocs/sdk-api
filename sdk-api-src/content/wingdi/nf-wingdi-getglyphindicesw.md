---
UID: NF:wingdi.GetGlyphIndicesW
title: GetGlyphIndicesW function (wingdi.h)
description: The GetGlyphIndices function translates a string into an array of glyph indices. The function can be used to determine whether a glyph exists in a font. (Unicode)
helpviewer_keywords: ["GGI_MARK_NONEXISTING_GLYPHS", "GetGlyphIndices", "GetGlyphIndices function [Windows GDI]", "GetGlyphIndicesW", "_win32_GetGlyphIndices", "gdi.getglyphindices", "wingdi/GetGlyphIndices", "wingdi/GetGlyphIndicesW"]
old-location: gdi\getglyphindices.htm
tech.root: gdi
ms.assetid: 7abfee7a-dd5d-4f33-96f1-b38364ba5afd
ms.date: 12/05/2018
ms.keywords: GGI_MARK_NONEXISTING_GLYPHS, GetGlyphIndices, GetGlyphIndices function [Windows GDI], GetGlyphIndicesA, GetGlyphIndicesW, _win32_GetGlyphIndices, gdi.getglyphindices, wingdi/GetGlyphIndices, wingdi/GetGlyphIndicesA, wingdi/GetGlyphIndicesW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetGlyphIndicesW (Unicode) and GetGlyphIndicesA (ANSI)
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
 - GetGlyphIndicesW
 - wingdi/GetGlyphIndicesW
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
 - GetGlyphIndices
 - GetGlyphIndicesA
 - GetGlyphIndicesW
---

# GetGlyphIndicesW function


## -description

The <b>GetGlyphIndices</b> function translates a string into an array of glyph indices. The function can be used to determine whether a glyph exists in a font.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpstr [in]

A pointer to the string to be converted.

### -param c [in]

The length of both the <a href="/windows/desktop/gdi/specifying-length-of-text-output-string">length of the string</a> pointed to by <i>lpstr</i> and the size (in WORDs) of the buffer pointed to by <i>pgi</i>.

### -param pgi [out]

This buffer must be of dimension c. On successful return, contains an array of glyph indices corresponding to the characters in the string.

### -param fl [in]

Specifies how glyphs should be handled if they are not supported. This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GGI_MARK_NONEXISTING_GLYPHS"></a><a id="ggi_mark_nonexisting_glyphs"></a><dl>
<dt><b>GGI_MARK_NONEXISTING_GLYPHS</b></dt>
</dl>
</td>
<td width="60%">
Marks unsupported glyphs with the hexadecimal value 0xffff.

</td>
</tr>
</table>

## -returns

If the function succeeds, it returns the number of bytes (for the ANSI function) or WORDs (for the Unicode function) converted.

If the function fails, the return value is GDI_ERROR.

## -remarks

This function attempts to identify a single-glyph representation for each character in the string pointed to by <i>lpstr</i>. While this is useful for certain low-level purposes (such as manipulating font files), higher-level applications that wish to map a string to glyphs will typically wish to use the <a href="/windows/desktop/Intl/uniscribe">Uniscribe</a> functions.





> [!NOTE]
> The wingdi.h header defines GetGlyphIndices as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getfontunicoderanges">GetFontUnicodeRanges</a>
