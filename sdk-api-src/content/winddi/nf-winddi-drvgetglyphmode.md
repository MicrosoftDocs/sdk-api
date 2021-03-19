---
UID: NF:winddi.DrvGetGlyphMode
title: DrvGetGlyphMode function (winddi.h)
description: The DrvGetGlyphMode function tells GDI how to cache glyph information.
helpviewer_keywords: ["DrvGetGlyphMode","DrvGetGlyphMode function [Display Devices]","ddifncs_e5ac278d-3417-4b76-aa0f-7fd2906f8137.xml","display.drvgetglyphmode","winddi/DrvGetGlyphMode"]
old-location: display\drvgetglyphmode.htm
tech.root: display
ms.assetid: 8e11c4e7-0203-4445-8f33-3b928161c62a
ms.date: 12/05/2018
ms.keywords: DrvGetGlyphMode, DrvGetGlyphMode function [Display Devices], ddifncs_e5ac278d-3417-4b76-aa0f-7fd2906f8137.xml, display.drvgetglyphmode, winddi/DrvGetGlyphMode
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
 - DrvGetGlyphMode
 - winddi/DrvGetGlyphMode
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
 - DrvGetGlyphMode
---

# DrvGetGlyphMode function


## -description

The <b>DrvGetGlyphMode</b> function tells GDI how to cache glyph information.

## -parameters

### -param unnamedParam1 [in]

Handle to a physical device's <a href="/windows-hardware/drivers/">PDEV</a> structure.

### -param unnamedParam2 [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure that can be queried to find the font size, transform, and other font attributes.

## -returns

<b>DrvGetGlyphMode</b> returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FO_GLYPHBITS</b></dt>
</dl>
</td>
<td width="60%">
GDI should cache all glyph data for this font.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FO_HGLYPHS</b></dt>
</dl>
</td>
<td width="60%">
The device caches fonts on its own, so GDI should cache only glyph handles for this font.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FO_PATHOBJ</b></dt>
</dl>
</td>
<td width="60%">
GDI should cache PATHOBJ structures for this font.

</td>
</tr>
</table>

## -remarks

GDI calls a driver's <b>DrvGetGlyphMode</b> routine to determine the range of font information that should be cached for a particular font; that is, <b>DrvGetGlyphMode</b> determines what GDI stores in its font cache. A device that caches fonts on its own should return FO_HGLYPHS to minimize the storage requirements for the font.

GDI calls <b>DrvGetGlyphMode</b> for each font realization. For example, a driver might want to download outlines for point sizes larger than 12 point, but raster images for smaller fonts. However, GDI reserves the right to refuse this request.

The driver must check the RASTER_FONTTYPE bit of the <b>flFontType</b> member of the FONTOBJ structure to determine the actual form of the glyphs. If this bit is set, GDI is sending bitmaps; otherwise it is sending <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structures.

At the time of the call to <b>DrvGetGlyphMode</b>, the associated FONTOBJ is not fully functional. GDI guarantees only that the <a href="/windows/desktop/api/winddi/ns-winddi-ifimetrics">IFIMETRICS</a> structure and the notional-to-device transform are correct.

<b>DrvGetGlyphMode</b> is an optional driver function. If this function is not provided, GDI will store raster fonts by default.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-fontobj_cgetglyphs">FONTOBJ_cGetGlyphs</a>



<a href="/windows/desktop/api/winddi/ns-winddi-glyphdef">GLYPHDEF</a>



<a href="/windows/desktop/api/winddi/ns-winddi-glyphpos">GLYPHPOS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-ifimetrics">IFIMETRICS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a>