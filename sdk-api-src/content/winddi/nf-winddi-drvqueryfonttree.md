---
UID: NF:winddi.DrvQueryFontTree
title: DrvQueryFontTree function (winddi.h)
description: The DrvQueryFontTree function provides GDI with a pointer to a structure that defines one of the following:A mapping from Unicode to glyph handles, including glyph variantsA mapping of kerning pairs to kerning handles
helpviewer_keywords: ["DrvQueryFontTree","DrvQueryFontTree function [Display Devices]","ddifncs_7f9eb5d2-dedd-4c72-8c12-0a382ea59ff4.xml","display.drvqueryfonttree","winddi/DrvQueryFontTree"]
old-location: display\drvqueryfonttree.htm
tech.root: display
ms.assetid: 29601ea6-9b68-4cdc-a7a1-b6a922524760
ms.date: 12/05/2018
ms.keywords: DrvQueryFontTree, DrvQueryFontTree function [Display Devices], ddifncs_7f9eb5d2-dedd-4c72-8c12-0a382ea59ff4.xml, display.drvqueryfonttree, winddi/DrvQueryFontTree
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
 - DrvQueryFontTree
 - winddi/DrvQueryFontTree
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
 - DrvQueryFontTree
---

# DrvQueryFontTree function


## -description

The <b>DrvQueryFontTree</b> function provides GDI with a pointer to a structure that defines one of the following:
<ul>
<li>
A mapping from Unicode to glyph handles, including glyph variants

</li>
<li>
A mapping of kerning pairs to kerning handles 

</li>
</ul>

## -parameters

### -param dhpdev

Identifies a device by a handle to its <a href="/windows-hardware/drivers/">PDEV</a>, returned from a prior call to <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>.

### -param iFile

Identifies the driver font file. This value is returned by <a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>.

### -param iFace

Specifies the one-based index of the driver font.

### -param iMode

Specifies the type of information to be provided. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
QFT_GLYPHSET

</td>
<td>
GDI requests a pointer to an <a href="/windows/desktop/api/winddi/ns-winddi-fd_glyphset">FD_GLYPHSET</a> structure that defines the mappings from single Unicode characters to glyph handles.

</td>
</tr>
<tr>
<td>
QFT_KERNPAIRS

</td>
<td>
GDI requests a pointer to a sorted, null-terminated array of <a href="/windows/desktop/api/winddi/ns-winddi-fd_kerningpair">FD_KERNINGPAIR</a> structures.

The kerning pairs should be stored in increasing order. The primary key is the second Unicode character; the secondary key is the first Unicode character in the kerning pair.

</td>
</tr>
</table>

### -param pid

Pointer to a memory location holding the address of a driver-defined value. GDI passes the contents of *<i>pid</i> to <a href="/windows/desktop/api/winddi/nf-winddi-drvfree">DrvFree</a>, along with the returned pointer, when the FD_GLYPHSET structure or array of FD_KERNINGPAIR structures are no longer needed. Depending on how memory is managed in the driver, the driver-defined value can identify the structure, identify the way it was allocated, or do nothing at all.

## -returns

The return value is a pointer to the requested structure if the function is successful. Otherwise, it is <b>NULL</b>, and an error code is logged.

## -remarks

The returned structure must remain unmodified until GDI calls <a href="/windows/desktop/api/winddi/nf-winddi-drvfree">DrvFree</a> with the address of the structure.

<b>DrvQueryFontTree</b> is required for font drivers and drivers that use device-specific fonts.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvfree">DrvFree</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfontdata">DrvQueryFontData</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfonttree">DrvQueryFontTree</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fd_glyphset">FD_GLYPHSET</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fd_kerningpair">FD_KERNINGPAIR</a>



<a href="/windows/desktop/api/winddi/ns-winddi-ifimetrics">IFIMETRICS</a>