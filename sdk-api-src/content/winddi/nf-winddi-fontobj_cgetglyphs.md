---
UID: NF:winddi.FONTOBJ_cGetGlyphs
title: FONTOBJ_cGetGlyphs function (winddi.h)
description: The FONTOBJ_cGetGlyphs function is a service to the font consumer that translates glyph handles into pointers to glyph data, which are valid until the next call to FONTOBJ_cGetGlyphs.
helpviewer_keywords: ["FONTOBJ_cGetGlyphs","FONTOBJ_cGetGlyphs function [Display Devices]","display.fontobj_cgetglyphs","gdifncs_8e402f9d-4ce3-4907-921c-9c0335a3966b.xml","winddi/FONTOBJ_cGetGlyphs"]
old-location: display\fontobj_cgetglyphs.htm
tech.root: display
ms.assetid: 0174fc88-e665-427e-b22f-468ddbea5b47
ms.date: 12/05/2018
ms.keywords: FONTOBJ_cGetGlyphs, FONTOBJ_cGetGlyphs function [Display Devices], display.fontobj_cgetglyphs, gdifncs_8e402f9d-4ce3-4907-921c-9c0335a3966b.xml, winddi/FONTOBJ_cGetGlyphs
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FONTOBJ_cGetGlyphs
 - winddi/FONTOBJ_cGetGlyphs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - FONTOBJ_cGetGlyphs
---

# FONTOBJ_cGetGlyphs function


## -description

The <b>FONTOBJ_cGetGlyphs</b> function is a service to the font consumer that translates glyph handles into pointers to glyph data, which are valid until the next call to <b>FONTOBJ_cGetGlyphs</b>.

## -parameters

### -param pfo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure containing the glyph handles to be translated.

### -param iMode [in]

Specifies whether data will be written as bitmaps or as outline objects. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FO_GLYPHBITS

</td>
<td>
Data will consist of <a href="/windows/desktop/api/winddi/ns-winddi-glyphbits">GLYPHBITS</a> structures that define the bitmaps of the glyphs.

</td>
</tr>
<tr>
<td>
FO_PATHOBJ

</td>
<td>
Data will consist of <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structures that define the outlines of the glyphs.

To determine whether the path should be filled or stroked, the font consumer should check the <b>flInfo</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-ifimetrics">IFIMETRICS</a> structure. If the FM_INFO_RETURNS_STROKES flag is set, the path should be stroked; otherwise, the path should be filled.

</td>
</tr>
</table>

### -param cGlyph

Specifies the number of glyphs to be translated. The only acceptable value is 1 (the code assumes 1, regardless of the value specified).

### -param phg

Pointer to an array of <i>cGlyph</i> HGLYPH structures supplied by the driver.

### -param ppvGlyph

Pointer to a memory location that receives the address of a <a href="/windows/desktop/api/winddi/ns-winddi-glyphdata">GLYPHDATA</a> structure. The first member of this structure is a <a href="/windows/desktop/api/winddi/ns-winddi-glyphdef">GLYPHDEF</a> union, which contains a pointer to either a GLYPHBITS structure or a PATHOBJ structure, depending on the value of the <i>iMode</i> parameter. If the value of <i>iMode</i> is FO_GLYPHBITS, (*<i>ppvGlyph)</i>-&gt;<i>gdf</i> contains the address of a GLYPHBITS structure. If the value of <i>iMode</i> is FO_PATHOBJ, (*<i>ppvGlyph</i>)-&gt;<i>gdf</i> contains the address of a PATHOBJ structure.

## -returns

The return value is the count of pointers passed to the driver if the function is successful. Otherwise, it is zero, and an error code is logged.

## -remarks

This function should be used if the driver is caching fonts.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvgetglyphmode">DrvGetGlyphMode</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-fontobj_cgetallglyphhandles">FONTOBJ_cGetAllGlyphHandles</a>



<a href="/windows/desktop/api/winddi/ns-winddi-glyphbits">GLYPHBITS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-ifimetrics">IFIMETRICS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>