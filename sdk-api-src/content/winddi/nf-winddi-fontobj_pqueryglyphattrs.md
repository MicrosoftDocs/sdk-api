---
UID: NF:winddi.FONTOBJ_pQueryGlyphAttrs
title: FONTOBJ_pQueryGlyphAttrs function (winddi.h)
description: The FONTOBJ_pQueryGlyphAttrs function returns information about a font's glyphs.
helpviewer_keywords: ["FONTOBJ_pQueryGlyphAttrs","FONTOBJ_pQueryGlyphAttrs function [Display Devices]","display.fontobj_pqueryglyphattrs","gdifncs_d646608d-3765-4cc7-aeff-bf5dc050d6b5.xml","winddi/FONTOBJ_pQueryGlyphAttrs"]
old-location: display\fontobj_pqueryglyphattrs.htm
tech.root: display
ms.assetid: 6a619922-5ab6-4169-8b41-e645e9d7fe93
ms.date: 12/05/2018
ms.keywords: FONTOBJ_pQueryGlyphAttrs, FONTOBJ_pQueryGlyphAttrs function [Display Devices], display.fontobj_pqueryglyphattrs, gdifncs_d646608d-3765-4cc7-aeff-bf5dc050d6b5.xml, winddi/FONTOBJ_pQueryGlyphAttrs
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
 - FONTOBJ_pQueryGlyphAttrs
 - winddi/FONTOBJ_pQueryGlyphAttrs
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
 - FONTOBJ_pQueryGlyphAttrs
---

# FONTOBJ_pQueryGlyphAttrs function


## -description

The <b>FONTOBJ_pQueryGlyphAttrs</b> function returns information about a font's glyphs.

## -parameters

### -param pfo

Is a caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure identifying the font for which attributes are being requested.

### -param iMode [in]

Is a caller-supplied flag indicating the type of glyph attribute being requested. The following flag is defined:

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
FO_ATTR_MODE_ROTATE

</td>
<td>
The function returns an array indicating which glyphs of a vertical font must be rotated.

</td>
</tr>
</table>

## -returns

<b>FONTOBJ_pQueryGlyphAttrs</b> returns a pointer to an <a href="/windows/desktop/api/winddi/ns-winddi-fd_glyphattr">FD_GLYPHATTR</a> structure. If an error is encountered, such as an invalid input argument, or if the font described by the <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure is not a vertical font, the function returns <b>NULL</b>.

## -remarks

Currently, the only attribute flag defined is FO_ATTR_MODE_ROTATE. This flag is meant for use by printer drivers that support printers with built-in font rasterizers. The driver can call the <b>FONTOBJ_pQueryGlyphAttrs</b> function, specifying the FO_ATTR_MODE_ROTATE flag, to determine which glyphs within a vertical font must be rotated.

Vertical fonts have a font name that starts with the "@" character. To determine if the current font is a vertical font, the driver can check for the FO_VERT_FACE flag in the <b>flFontType</b> member of the font's <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure.

Rotation information is returned in the <a href="/windows/desktop/api/winddi/ns-winddi-fd_glyphattr">FD_GLYPHATTR</a> structure that is used as the function's return value.

The <b>FONTOBJ_pQueryGlyphAttrs</b> function is supplied by GDI. When a printer driver calls <b>FONTOBJ_pQueryGlyphAttrs</b>, GDI calls the appropriate font driver's <a href="/windows/desktop/api/winddi/nc-winddi-pfn_drvqueryglyphattrs">DrvQueryGlyphAttrs</a> function to obtain the requested information.

## -see-also

<a href="/windows/desktop/api/winddi/nc-winddi-pfn_drvqueryglyphattrs">DrvQueryGlyphAttrs</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fd_glyphattr">FD_GLYPHATTR</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>