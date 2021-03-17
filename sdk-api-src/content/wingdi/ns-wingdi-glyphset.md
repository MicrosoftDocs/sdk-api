---
UID: NS:wingdi.tagGLYPHSET
title: GLYPHSET (wingdi.h)
description: The GLYPHSET structure contains information about a range of Unicode code points.
helpviewer_keywords: ["*LPGLYPHSET","*PGLYPHSET","GLYPHSET","GLYPHSET structure [Windows GDI]","PGLYPHSET","PGLYPHSET structure pointer [Windows GDI]","_win32_GLYPHSET_str","gdi.glyphset","wingdi/GLYPHSET","wingdi/PGLYPHSET"]
old-location: gdi\glyphset.htm
tech.root: gdi
ms.assetid: b8ac8d3f-b062-491c-966f-02f3d4c11419
ms.date: 12/05/2018
ms.keywords: '*LPGLYPHSET, *PGLYPHSET, GLYPHSET, GLYPHSET structure [Windows GDI], PGLYPHSET, PGLYPHSET structure pointer [Windows GDI], _win32_GLYPHSET_str, gdi.glyphset, wingdi/GLYPHSET, wingdi/PGLYPHSET'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: GLYPHSET, *PGLYPHSET, *LPGLYPHSET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagGLYPHSET
 - wingdi/tagGLYPHSET
 - PGLYPHSET
 - wingdi/PGLYPHSET
 - GLYPHSET
 - wingdi/GLYPHSET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - GLYPHSET
---

# GLYPHSET structure


## -description

The <b>GLYPHSET</b> structure contains information about a range of Unicode code points.

## -struct-fields

### -field cbThis

The size, in bytes, of this structure.

### -field flAccel

Flags describing the maximum size of the glyph indices. This member can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>GS_8BIT_INDICES</td>
<td>Treat glyph indices as 8-bit wide values. Otherwise, they are 16-bit wide values.</td>
</tr>
</table>

### -field cGlyphsSupported

The total number of Unicode code points supported in the font.

### -field cRanges

The total number of Unicode ranges in <b>ranges</b>.

### -field ranges

Array of Unicode ranges that are supported in the font.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-structures">Font and Text Structures</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getfontunicoderanges">GetFontUnicodeRanges</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-wcrange">WCRANGE</a>