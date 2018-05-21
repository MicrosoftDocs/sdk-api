---
UID: NF:wingdi.GetGlyphOutlineA
title: GetGlyphOutlineA function
author: windows-driver-content
description: The GetGlyphOutline function retrieves the outline or bitmap for a character in the TrueType font that is selected into the specified device context.
old-location: gdi\getglyphoutline.htm
old-project: gdi
ms.assetid: 08f06007-5b21-44ab-b234-21a58c94ed4e
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GGO_BEZIER, GGO_BITMAP, GGO_GLYPH_INDEX, GGO_GRAY2_BITMAP, GGO_GRAY4_BITMAP, GGO_GRAY8_BITMAP, GGO_METRICS, GGO_NATIVE, GGO_UNHINTED, GetGlyphOutline, GetGlyphOutline function [Windows GDI], GetGlyphOutlineA, GetGlyphOutlineW, _win32_GetGlyphOutline, gdi.getglyphoutline, wingdi/GetGlyphOutline, wingdi/GetGlyphOutlineA, wingdi/GetGlyphOutlineW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Font-l1-1-1.dll
-	ext-ms-win-gdi-font-l1-1-2.dll
-	Ext-MS-Win-GDI-Font-L1-1-3.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	GetGlyphOutline
-	GetGlyphOutlineA
-	GetGlyphOutlineW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetGlyphOutlineA function


## -description


The <b>GetGlyphOutline</b> function retrieves the outline or bitmap for a character in the TrueType font that is selected into the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param uChar [in]

The character for which data is to be returned.


### -param fuFormat

TBD


### -param lpgm [out]

A pointer to the <a href="https://msdn.microsoft.com/a6fa3813-56f7-4b54-b21d-8aabc2309a34">GLYPHMETRICS</a> structure describing the placement of the glyph in the character cell.


### -param cjBuffer

TBD


### -param pvBuffer

TBD


### -param lpmat2 [in]

A pointer to a <a href="https://msdn.microsoft.com/841883d6-bc4d-46ef-abf4-f179771d255b">MAT2</a> structure specifying a transformation matrix for the character.


#### - cbBuffer [in]

The size, in bytes, of the buffer (*<i>lpvBuffer</i>) where the function is to copy information about the outline character. If this value is zero, the function returns the required size of the buffer.


#### - lpvBuffer [out]

A pointer to the buffer that receives information about the outline character. If this value is <b>NULL</b>, the function returns the required size of the buffer.


#### - uFormat [in]

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
Indicates that the <i>uChar</i> parameter is a TrueType Glyph Index rather than a character code. See the <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> function for additional remarks on Glyph Indexing.

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
The function only retrieves the <a href="https://msdn.microsoft.com/a6fa3813-56f7-4b54-b21d-8aabc2309a34">GLYPHMETRICS</a> structure specified by <i>lpgm</i>. The <i>lpvBuffer</i> is ignored. This value affects the meaning of the function's return value upon failure; see the Return Values section.

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


## -returns



If GGO_BITMAP, GGO_GRAY2_BITMAP, GGO_GRAY4_BITMAP, GGO_GRAY8_BITMAP, or GGO_NATIVE is specified and the function succeeds, the return value is greater than zero; otherwise, the return value is GDI_ERROR. If one of these flags is specified and the buffer size or address is zero, the return value specifies the required buffer size, in bytes.

If GGO_METRICS is specified and the function fails, the return value is GDI_ERROR.




## -remarks



The glyph outline returned by the <b>GetGlyphOutline</b> function is for a grid-fitted glyph. (A grid-fitted glyph is a glyph that has been modified so that its bitmapped image conforms as closely as possible to the original design of the glyph.) If an application needs an unmodified glyph outline, it can request the glyph outline for a character in a font whose size is equal to the font's em unit. The value for a font's em unit is stored in the <b>otmEMSquare</b> member of the <a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a> structure.

The glyph bitmap returned by <b>GetGlyphOutline</b> when GGO_BITMAP is specified is a DWORD-aligned, row-oriented, monochrome bitmap. When GGO_GRAY2_BITMAP is specified, the bitmap returned is a DWORD-aligned, row-oriented array of bytes whose values range from 0 to 4. When GGO_GRAY4_BITMAP is specified, the bitmap returned is a DWORD-aligned, row-oriented array of bytes whose values range from 0 to 16. When GGO_GRAY8_BITMAP is specified, the bitmap returned is a DWORD-aligned, row-oriented array of bytes whose values range from 0 to 64.

The native buffer returned by <b>GetGlyphOutline</b> when GGO_NATIVE is specified is a glyph outline. A glyph outline is returned as a series of one or more contours defined by a <a href="https://msdn.microsoft.com/eea54aeb-7847-4393-87fa-86de93017be8">TTPOLYGONHEADER</a> structure followed by one or more curves. Each curve in the contour is defined by a <a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a> structure followed by a number of <a href="https://msdn.microsoft.com/a8736c6c-7944-42ed-811c-308f41f1ab2f">POINTFX</a> data points. <b>POINTFX</b> points are absolute positions, not relative moves. The starting point of a contour is given by the <b>pfxStart</b> member of the <b>TTPOLYGONHEADER</b> structure. The starting point of each curve is the last point of the previous curve or the starting point of the contour. The count of data points in a curve is stored in the <b>cpfx</b> member of <b>TTPOLYCURVE</b> structure. The size of each contour in the buffer, in bytes, is stored in the <b>cb</b> member of <b>TTPOLYGONHEADER</b> structure. Additional curve definitions are packed into the buffer following preceding curves and additional contours are packed into the buffer following preceding contours. The buffer contains as many contours as fit within the buffer returned by <b>GetGlyphOutline</b>.

The <a href="https://msdn.microsoft.com/a6fa3813-56f7-4b54-b21d-8aabc2309a34">GLYPHMETRICS</a> structure specifies the width of the character cell and the location of a glyph within the character cell. The origin of the character cell is located at the left side of the cell at the baseline of the font. The location of the glyph origin is relative to the character cell origin. The height of a character cell, the baseline, and other metrics global to the font are given by the <a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a> structure.

An application can alter the characters retrieved in bitmap or native format by specifying a 2-by-2 transformation matrix in the <i>lpMatrix</i> parameter. For example the glyph can be modified by shear, rotation, scaling, or any combination of the three using matrix multiplication.

Additional information on a glyph outlines is located in the TrueType and the OpenType technical specifications.




## -see-also




<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>



<a href="https://msdn.microsoft.com/1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7">FORM_INFO_1</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/a6fa3813-56f7-4b54-b21d-8aabc2309a34">GLYPHMETRICS</a>



<a href="https://msdn.microsoft.com/b8c7a557-ca35-41a4-9043-8496e5b01564">GetOutlineTextMetrics</a>



<a href="https://msdn.microsoft.com/841883d6-bc4d-46ef-abf4-f179771d255b">MAT2</a>



<a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<a href="https://msdn.microsoft.com/a8736c6c-7944-42ed-811c-308f41f1ab2f">POINTFX</a>



<a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a>



<a href="https://msdn.microsoft.com/eea54aeb-7847-4393-87fa-86de93017be8">TTPOLYGONHEADER</a>
 

 

