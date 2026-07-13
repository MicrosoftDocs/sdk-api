---
UID: NF:winddi.EngComputeGlyphSet
title: EngComputeGlyphSet function (winddi.h)
description: The EngComputeGlyphSet function computes the glyph set supported on a device.
helpviewer_keywords: ["EngComputeGlyphSet","EngComputeGlyphSet function [Display Devices]","display.engcomputeglyphset","gdifncs_ba8356d5-4114-436c-9268-774b8e0918df.xml","winddi/EngComputeGlyphSet"]
old-location: display\engcomputeglyphset.htm
tech.root: display
ms.assetid: 74722493-04cf-4401-a6d6-7afe8d4881d9
ms.date: 12/05/2018
ms.keywords: EngComputeGlyphSet, EngComputeGlyphSet function [Display Devices], display.engcomputeglyphset, gdifncs_ba8356d5-4114-436c-9268-774b8e0918df.xml, winddi/EngComputeGlyphSet
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
 - EngComputeGlyphSet
 - winddi/EngComputeGlyphSet
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngComputeGlyphSet
---

# EngComputeGlyphSet function


## -description

The <b>EngComputeGlyphSet</b> function computes the glyph set supported on a device.

## -parameters

### -param nCodePage [in]

Specifies the code page supported.

### -param nFirstChar [in]

Specifies the character code of the first supported ANSI character.

### -param cChars [in]

Specifies the number of ANSI characters supported.

## -returns

If the glyph set is computed successfully, the function returns a pointer to an <a href="/windows/desktop/api/winddi/ns-winddi-fd_glyphset">FD_GLYPHSET</a> structure. If an error occurs, the function returns <b>NULL</b>.

## -remarks

A driver can use <b>EngComputeGlyphSet</b> to compute the glyph set for a font that contains only glyphs in the code page described by <i>nCodePage</i>.

The driver must call <a href="/windows/desktop/api/winddi/nf-winddi-engfreemem">EngFreeMem</a> to free memory when it is done using the FD_GLYPHSET structure returned by <b>EngComputeGlyphSet</b>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engfreemem">EngFreeMem</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fd_glyphset">FD_GLYPHSET</a>