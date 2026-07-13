---
UID: NF:wingdi.GetGlyphOutlineA
title: GetGlyphOutlineA function (wingdi.h)
description: The GetGlyphOutline function retrieves the outline or bitmap for a character in the TrueType font that is selected into the specified device context. (ANSI)
helpviewer_keywords: ["GGO_BEZIER", "GGO_BITMAP", "GGO_GLYPH_INDEX", "GGO_GRAY2_BITMAP", "GGO_GRAY4_BITMAP", "GGO_GRAY8_BITMAP", "GGO_METRICS", "GGO_NATIVE", "GGO_UNHINTED", "GetGlyphOutlineA", "wingdi/GetGlyphOutlineA"]
old-location: gdi\getglyphoutline.htm
tech.root: gdi
ms.assetid: 08f06007-5b21-44ab-b234-21a58c94ed4e
ms.date: 12/05/2018
ms.keywords: GGO_BEZIER, GGO_BITMAP, GGO_GLYPH_INDEX, GGO_GRAY2_BITMAP, GGO_GRAY4_BITMAP, GGO_GRAY8_BITMAP, GGO_METRICS, GGO_NATIVE, GGO_UNHINTED, GetGlyphOutline, GetGlyphOutline function [Windows GDI], GetGlyphOutlineA, GetGlyphOutlineW, _win32_GetGlyphOutline, gdi.getglyphoutline, wingdi/GetGlyphOutline, wingdi/GetGlyphOutlineA, wingdi/GetGlyphOutlineW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetGlyphOutlineW (Unicode) and GetGlyphOutlineA (ANSI)
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
 - GetGlyphOutlineA
 - wingdi/GetGlyphOutlineA
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
 - GetGlyphOutline
 - GetGlyphOutlineA
 - GetGlyphOutlineW
---

# GetGlyphOutlineA function


## -description

The <b>GetGlyphOutline</b> function retrieves the outline or bitmap for a character in the TrueType font that is selected into the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param uChar [in]

The character for which data is to be returned.

### -param fuFormat [in]

The format of the data that the function retrieves. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GGO_BEZIER"></a><a id="ggo_bezier"></a><dl>
<dt><b>GGO_BEZIER</b></dt>
</dl>
</td>
<td width="60%">
The function retrieves the curve data as a cubic Bézier spline (not in quadratic spline format).

</td>
</tr>
<tr>
<td width="40%"><a id="GGO_BITMAP"></a><a id="ggo_bitmap"></a><dl>
<dt><b>GGO_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
The function retrieves the glyph bitmap. For information about memory allocation, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="GGO_GLYPH_INDEX"></a><a id="ggo_glyph_index"></a><dl>
<dt><b>GGO_GLYPH_INDEX</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <i>uChar</i> parameter is a TrueType Glyph Index rather than a character code. See the <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> function for additional remarks on Glyph Indexing.

</td>
</tr>
<tr>
<td width="40%"><a id="GGO_GRAY2_BITMAP"></a><a id="ggo_gray2_bitmap"></a><dl>
<dt><b>GGO_GRAY2_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
The function retrieves a glyph bitmap that contains five levels of gray.

</td>
</tr>
<tr>
<td width="40%"><a id="GGO_GRAY4_BITMAP"></a><a id="ggo_gray4_bitmap"></a><dl>
<dt><b>GGO_GRAY4_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
The function retrieves a glyph bitmap that contains 17 levels of gray.

</td>
</tr>
<tr>
<td width="40%"><a id="GGO_GRAY8_BITMAP"></a><a id="ggo_gray8_bitmap"></a><dl>
<dt><b>GGO_GRAY8_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
The function retrieves a glyph bitmap that contains 65 levels of gray.

</td>
</tr>
<tr>
<td width="40%"><a id="GGO_METRICS"></a><a id="ggo_metrics"></a><dl>
<dt><b>GGO_METRICS</b></dt>
</dl>
</td>
<td width="60%">
The function only retrieves the <a href="/windows/desktop/api/wingdi/ns-wingdi-glyphmetrics">GLYPHMETRICS</a> structure specified by <i>lpgm</i>. The <i>lpvBuffer</i> is ignored. This value affects the meaning of the function's return value upon failure; see the Return Values section.

</td>
</tr>
<tr>
<td width="40%"><a id="GGO_NATIVE"></a><a id="ggo_native"></a><dl>
<dt><b>GGO_NATIVE</b></dt>
</dl>
</td>
<td width="60%">
The function retrieves the curve data points in the rasterizer's native format and uses the font's design units.

</td>
</tr>
<tr>
<td width="40%"><a id="GGO_UNHINTED"></a><a id="ggo_unhinted"></a><dl>
<dt><b>GGO_UNHINTED</b></dt>
</dl>
</td>
<td width="60%">
The function only returns unhinted outlines. This flag only works in conjunction with GGO_BEZIER and GGO_NATIVE.

</td>
</tr>
</table>
 

Note that, for the GGO_GRAYn_BITMAP values, the function retrieves a glyph bitmap that contains n^2+1 (n squared plus one) levels of gray.

### -param lpgm [out]

A pointer to the <a href="/windows/desktop/api/wingdi/ns-wingdi-glyphmetrics">GLYPHMETRICS</a> structure describing the placement of the glyph in the character cell.

### -param cjBuffer [in]

The size, in bytes, of the buffer (*<i>lpvBuffer</i>) where the function is to copy information about the outline character. If this value is zero, the function returns the required size of the buffer.

### -param pvBuffer [out]

A pointer to the buffer that receives information about the outline character. If this value is <b>NULL</b>, the function returns the required size of the buffer.

### -param lpmat2 [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-mat2">MAT2</a> structure specifying a transformation matrix for the character.

## -returns

If GGO_BITMAP, GGO_GRAY2_BITMAP, GGO_GRAY4_BITMAP, GGO_GRAY8_BITMAP, or GGO_NATIVE is specified and the function succeeds, the return value is greater than zero; otherwise, the return value is GDI_ERROR. If one of these flags is specified and the buffer size or address is zero, the return value specifies the required buffer size, in bytes.

If GGO_METRICS is specified and the function fails, the return value is GDI_ERROR.

## -remarks

The glyph outline returned by the <b>GetGlyphOutline</b> function is for a grid-fitted glyph. (A grid-fitted glyph is a glyph that has been modified so that its bitmapped image conforms as closely as possible to the original design of the glyph.) If an application needs an unmodified glyph outline, it can request the glyph outline for a character in a font whose size is equal to the font's em unit. The value for a font's em unit is stored in the <b>otmEMSquare</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a> structure.

The glyph bitmap returned by <b>GetGlyphOutline</b> when GGO_BITMAP is specified is a DWORD-aligned, row-oriented, monochrome bitmap. When GGO_GRAY2_BITMAP is specified, the bitmap returned is a DWORD-aligned, row-oriented array of bytes whose values range from 0 to 4. When GGO_GRAY4_BITMAP is specified, the bitmap returned is a DWORD-aligned, row-oriented array of bytes whose values range from 0 to 16. When GGO_GRAY8_BITMAP is specified, the bitmap returned is a DWORD-aligned, row-oriented array of bytes whose values range from 0 to 64.

The native buffer returned by <b>GetGlyphOutline</b> when GGO_NATIVE is specified is a glyph outline. A glyph outline is returned as a series of one or more contours defined by a <a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolygonheader">TTPOLYGONHEADER</a> structure followed by one or more curves. Each curve in the contour is defined by a <a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolycurve">TTPOLYCURVE</a> structure followed by a number of <a href="/windows/desktop/api/wingdi/ns-wingdi-pointfx">POINTFX</a> data points. <b>POINTFX</b> points are absolute positions, not relative moves. The starting point of a contour is given by the <b>pfxStart</b> member of the <b>TTPOLYGONHEADER</b> structure. The starting point of each curve is the last point of the previous curve or the starting point of the contour. The count of data points in a curve is stored in the <b>cpfx</b> member of <b>TTPOLYCURVE</b> structure. The size of each contour in the buffer, in bytes, is stored in the <b>cb</b> member of <b>TTPOLYGONHEADER</b> structure. Additional curve definitions are packed into the buffer following preceding curves and additional contours are packed into the buffer following preceding contours. The buffer contains as many contours as fit within the buffer returned by <b>GetGlyphOutline</b>.

The <a href="/windows/desktop/api/wingdi/ns-wingdi-glyphmetrics">GLYPHMETRICS</a> structure specifies the width of the character cell and the location of a glyph within the character cell. The origin of the character cell is located at the left side of the cell at the baseline of the font. The location of the glyph origin is relative to the character cell origin. The height of a character cell, the baseline, and other metrics global to the font are given by the <a href="/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a> structure.

An application can alter the characters retrieved in bitmap or native format by specifying a 2-by-2 transformation matrix in the <i>lpMatrix</i> parameter. For example the glyph can be modified by shear, rotation, scaling, or any combination of the three using matrix multiplication.

Additional information on a glyph outlines is located in the TrueType and the OpenType technical specifications.





> [!NOTE]
> The wingdi.h header defines GetGlyphOutline as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="/windows/desktop/printdocs/form-info-1">FORM_INFO_1</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-glyphmetrics">GLYPHMETRICS</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getoutlinetextmetricsa">GetOutlineTextMetrics</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-mat2">MAT2</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-outlinetextmetrica">OUTLINETEXTMETRIC</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pointfx">POINTFX</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolycurve">TTPOLYCURVE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-ttpolygonheader">TTPOLYGONHEADER</a>
