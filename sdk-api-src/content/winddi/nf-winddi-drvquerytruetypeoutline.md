---
UID: NF:winddi.DrvQueryTrueTypeOutline
title: DrvQueryTrueTypeOutline function (winddi.h)
description: The DrvQueryTrueTypeOutline function retrieves glyph outlines in native TrueType format.
helpviewer_keywords: ["DrvQueryTrueTypeOutline","DrvQueryTrueTypeOutline function [Display Devices]","ddifncs_77215092-0dde-45d4-93f2-11a7b9e69360.xml","display.drvquerytruetypeoutline","winddi/DrvQueryTrueTypeOutline"]
old-location: display\drvquerytruetypeoutline.htm
tech.root: display
ms.assetid: 49123a0c-5096-4a0f-9444-2018b49b2010
ms.date: 12/05/2018
ms.keywords: DrvQueryTrueTypeOutline, DrvQueryTrueTypeOutline function [Display Devices], ddifncs_77215092-0dde-45d4-93f2-11a7b9e69360.xml, display.drvquerytruetypeoutline, winddi/DrvQueryTrueTypeOutline
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
 - DrvQueryTrueTypeOutline
 - winddi/DrvQueryTrueTypeOutline
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
 - DrvQueryTrueTypeOutline
---

# DrvQueryTrueTypeOutline function


## -description

The <b>DrvQueryTrueTypeOutline</b> function retrieves glyph outlines in native TrueType format.

## -parameters

### -param dhpdev

Handle to a physical device's <a href="/windows-hardware/drivers/">PDEV</a> structure returned from a call to <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>.

### -param pfo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure. Details of the font realization can be queried from this structure.

### -param hglyph

Handle to the glyph for which the outline is being queried.

### -param bMetricsOnly

Specifies that font metrics (only) should be returned, or that TrueType outlines should be returned in cubic Bezier format, or that the TrueType outlines should be returned unhinted. This value can be one of the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
TTO_METRICS_ONLY

</td>
<td>
Only font metrics are to be returned. Font data (either outlines or bitmaps) will not be returned.

</td>
</tr>
<tr>
<td>
TTO_QUBICS

</td>
<td>
Outlines are to be returned in cubic Bezier format.

</td>
</tr>
<tr>
<td>
TTO_UNHINTED

</td>
<td>
Outlines are to be returned unhinted.

</td>
</tr>
</table>

### -param pgldt

Pointer to the buffer where the <a href="/windows/desktop/api/winddi/ns-winddi-glyphdata">GLYPHDATA</a> structure for this glyph should be written. If <i>pgldt</i> is <b>NULL</b>, no data is written to the GLYPHDATA structure.

### -param cjBuf

Specifies the size, in bytes, of the buffer that receives the TrueType outline.

### -param ppoly

Pointer to the buffer where the TrueType outline should be written. The format of the data is in native TrueType format, stored in a TTPOLYGONHEADER structure. See the Microsoft Windows SDK documentation for more information about the TTPOLYGONHEADER structure.

## -returns

The return value is the size, in bytes, required for the <i>ppoly</i> buffer if <i>pgldt</i> is <b>NULL</b>. If <i>pgldt</i> is not <b>NULL</b>, the return value is the number of bytes copied into the <i>ppoly</i> buffer. If an error occurs, the return value is FD_ERROR.

## -remarks

<b>DrvQueryTrueTypeOutline</b> is required for TrueType font drivers.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>