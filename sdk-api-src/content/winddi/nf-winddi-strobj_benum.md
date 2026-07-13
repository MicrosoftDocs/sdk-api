---
UID: NF:winddi.STROBJ_bEnum
title: STROBJ_bEnum function (winddi.h)
description: The STROBJ_bEnum function enumerates glyph identities and positions.
helpviewer_keywords: ["STROBJ_bEnum","STROBJ_bEnum function [Display Devices]","display.strobj_benum","gdifncs_2925a0a5-f797-41a5-b5b1-d87d60d44905.xml","winddi/STROBJ_bEnum"]
old-location: display\strobj_benum.htm
tech.root: display
ms.assetid: 82cb12ff-2baa-4291-849c-dab9d01fa39b
ms.date: 12/05/2018
ms.keywords: STROBJ_bEnum, STROBJ_bEnum function [Display Devices], display.strobj_benum, gdifncs_2925a0a5-f797-41a5-b5b1-d87d60d44905.xml, winddi/STROBJ_bEnum
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
 - STROBJ_bEnum
 - winddi/STROBJ_bEnum
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
 - STROBJ_bEnum
---

# STROBJ_bEnum function


## -description

The <b>STROBJ_bEnum</b> function enumerates glyph identities and positions.

## -parameters

### -param pstro

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a> structure containing the <a href="/windows/desktop/api/winddi/ns-winddi-glyphpos">GLYPHPOS</a> information.

### -param pc

Pointer to the count, returned by GDI, of GLYPHPOS structures.

### -param ppgpos

Pointer to the array in which GDI writes the GLYPHPOS structures.

## -returns

The return value is <b>TRUE</b> if more glyphs remain to be enumerated, or <b>FALSE</b> if the enumeration is complete. The return value is DDI_ERROR if the glyphs cannot be enumerated, and an error code is logged.

## -remarks

A driver should download only the glyph handles if it caches fonts itself.

The information returned depends on the driver's return value for <a href="/windows/desktop/api/winddi/nf-winddi-drvgetglyphmode">DrvGetGlyphMode</a>. 

Bitmaps or outlines can also be obtained from <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structures.

Printer drivers should call <a href="/windows/desktop/api/winddi/nf-winddi-strobj_benumpositionsonly">STROBJ_bEnumPositionsOnly</a> instead of <b>STROBJ_bEnum</b> if printer hardware provides internal rendering of TrueType fonts.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvgetglyphmode">DrvGetGlyphMode</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-fontobj_cgetglyphs">FONTOBJ_cGetGlyphs</a>



<a href="/windows/desktop/api/winddi/ns-winddi-glyphpos">GLYPHPOS</a>



<a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-strobj_benumpositionsonly">STROBJ_bEnumPositionsOnly</a>



<a href="/windows/desktop/api/winddi/nf-winddi-strobj_venumstart">STROBJ_vEnumStart</a>