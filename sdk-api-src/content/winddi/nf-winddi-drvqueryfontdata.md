---
UID: NF:winddi.DrvQueryFontData
title: DrvQueryFontData function (winddi.h)
description: The DrvQueryFontData function retrieves information about a realized font.
helpviewer_keywords: ["DrvQueryFontData","DrvQueryFontData function [Display Devices]","ddifncs_6992339b-a8e8-4bdf-b7a4-7a3087f62051.xml","display.drvqueryfontdata","winddi/DrvQueryFontData"]
old-location: display\drvqueryfontdata.htm
tech.root: display
ms.assetid: 3f6efd3c-3ddf-4ce6-9527-730e01c45e74
ms.date: 12/05/2018
ms.keywords: DrvQueryFontData, DrvQueryFontData function [Display Devices], ddifncs_6992339b-a8e8-4bdf-b7a4-7a3087f62051.xml, display.drvqueryfontdata, winddi/DrvQueryFontData
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvQueryFontData
 - winddi/DrvQueryFontData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvQueryFontData
---

# DrvQueryFontData function


## -description

The <b>DrvQueryFontData</b> function retrieves information about a realized font.

## -parameters

### -param dhpdev

Handle to the physical device's <a href="/windows-hardware/drivers/">PDEV</a> that was returned from a prior call to <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>.

### -param pfo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure that defines the font realization.

### -param iMode

Specifies the type of information requested. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
QFD_GLYPHANDBITMAP

</td>
<td>
If <i>pgd</i> is not <b>NULL</b>, then the driver should fill in the <a href="/windows/desktop/api/winddi/ns-winddi-glyphdata">GLYPHDATA</a> structure with the metrics of the glyph specified by <i>hg</i>.

If <i>pv</i> is not <b>NULL</b>, a <a href="/windows/desktop/api/winddi/ns-winddi-glyphbits">GLYPHBITS</a> structure should be written at this address. The driver should copy the glyph bitmap corresponding to the glyph specified by <i>hg</i> into this structure. The size of the structure is specified by <i>cjSize</i>.

If glyph bitmaps are not supported by the driver, this function will only be called with <i>pv</i> set to <b>NULL</b>.

If the driver supports glyph bitmaps, the return value is the size, in bytes, of the glyph bitmap. Otherwise, it is zero.

This mode must be supported.

</td>
</tr>
<tr>
<td>
QFD_GLYPHANDOUTLINE

</td>
<td>
If <i>pgd</i> is not <b>NULL</b>, then the driver should fill in the <a href="/windows/desktop/api/winddi/ns-winddi-glyphdata">GLYPHDATA</a> structure with the metrics of the glyph specified by <i>hg</i>.

If <i>pv</i> is not <b>NULL</b>, a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure should be written at this address. The driver passes this PATHOBJ to the PATHOBJ_<i>Xxx</i> services to create the outline for the glyph specified by <i>hg</i>. The <i>cjSize</i> parameter should be ignored.

The return value is zero if the function is successful. Otherwise, it is FD_ERROR.

Only font drivers that provide glyph outlines need to support this mode.

</td>
</tr>
<tr>
<td>
QFD_MAXEXTENTS

</td>
<td>
If <i>pv</i> is not <b>NULL</b>, the driver should write an <a href="/windows/desktop/api/winddi/ns-winddi-fd_devicemetrics">FD_DEVICEMETRICS</a> structure to the buffer pointed to by <i>pv</i>.

The return value is the size, in bytes, needed for the buffer if <i>pv</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td>
QFD_TT_GRAY1_BITMAP

</td>
<td>
The realized font should be rendered in one bit-per-pixel of grayscale (that is, either black or white).

</td>
</tr>
<tr>
<td>
QFD_TT_GRAY2_BITMAP

</td>
<td>
The realized font should be rendered in two bits-per-pixel of grayscale.

</td>
</tr>
<tr>
<td>
QFD_TT_GRAY4_BITMAP

</td>
<td>
The realized font should be rendered in four bits-per-pixel of grayscale.

</td>
</tr>
<tr>
<td>
QFD_TT_GRAY8_BITMAP

</td>
<td>
The realized font should be rendered in eight bits-per-pixel of grayscale.

</td>
</tr>
<tr>
<td>
QFD_TT_MONO_BITMAP

</td>
<td>
Same as QFD_TT_GRAY1_BITMAP.

</td>
</tr>
</table>

### -param hg

Handle to the glyph.

### -param pgd

Pointer to <a href="/windows/desktop/api/winddi/ns-winddi-glyphdata">GLYPHDATA</a> structure. This parameter can be <b>NULL</b>.

### -param pv [out]

Pointer to a data buffer. The type of data written to this buffer is dependent on <i>iMode</i>. This parameter can be <b>NULL</b>.

### -param cjSize

Specifies the size of the buffer pointed to by <i>pv</i>.

## -returns

The return value depends on the value of the <i>iMode</i> parameter. If an error occurs, the return value is FD_ERROR, and an error code is logged.

## -remarks

For the QFD_GLYPHANDBITMAP and QFD_GLYPHANDOUTLINE values of the <i>iMode</i> parameter, GDI provides a pointer to a GLYPHDATA structure (in the <i>pgd</i> parameter). The driver places information about glyph metrics in this structure and writes the contents of either a GLYPHBITS structure or a PATHOBJ structure in the location specified by the <i>pv</i> parameter, depending respectively, on whether the font is a bitmap font or an outline font. For the QFD_MAXEXTENTS value of the <i>iMode</i> parameter, the driver writes the contents of an FD_DEVICEMETRICS structure in the location specified by the <i>pv</i> parameter. 

<b>DrvQueryFontData</b> is required for font drivers and drivers that use device-specific or driver-specific fonts.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfontfile">DrvQueryFontFile</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fd_devicemetrics">FD_DEVICEMETRICS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-glyphbits">GLYPHBITS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-glyphdata">GLYPHDATA</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>