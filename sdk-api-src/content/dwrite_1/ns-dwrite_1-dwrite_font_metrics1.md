---
UID: NS:dwrite_1.DWRITE_FONT_METRICS1
title: DWRITE_FONT_METRICS1 (dwrite_1.h)
description: The DWRITE_FONT_METRICS1 structure specifies the metrics that are applicable to all glyphs within the font face.
helpviewer_keywords: ["DWRITE_FONT_METRICS1","DWRITE_FONT_METRICS1 structure [Direct Write]","directwrite.dwrite_font_metrics1","dwrite_1/DWRITE_FONT_METRICS1"]
old-location: directwrite\dwrite_font_metrics1.htm
tech.root: DirectWrite
ms.assetid: F06033F4-2312-48C2-AF70-BDB83700B4E0
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_METRICS1, DWRITE_FONT_METRICS1 structure [Direct Write], directwrite.dwrite_font_metrics1, dwrite_1/DWRITE_FONT_METRICS1
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - DWRITE_FONT_METRICS1
 - dwrite_1/DWRITE_FONT_METRICS1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_FONT_METRICS1
---

# DWRITE_FONT_METRICS1 structure


## -description

The <b>DWRITE_FONT_METRICS1</b> structure specifies the metrics that are applicable to all glyphs within the font face.

## -struct-fields

### -field glyphBoxLeft

Left edge of accumulated bounding blackbox of all glyphs in the font.

### -field glyphBoxTop

Top edge of accumulated bounding blackbox of all glyphs in the font.

### -field glyphBoxRight

Right edge of accumulated bounding blackbox of all glyphs in the font.

### -field glyphBoxBottom

Bottom edge of accumulated bounding blackbox of all glyphs in the font.

### -field subscriptPositionX

Horizontal position of the subscript relative to the baseline origin. This is typically negative (to the left) in italic and oblique fonts, and zero in regular fonts.

### -field subscriptPositionY

Vertical position of the subscript relative to the baseline. This is typically negative.

### -field subscriptSizeX

Horizontal size of the subscript em box in design units, used to scale the simulated subscript relative to the full em box size. This is the numerator of the scaling ratio where denominator is the design units per em. If this member is zero, the font does not specify a scale factor, and the client uses its own policy.

### -field subscriptSizeY

Vertical size of the subscript em box in design units, used to scale the simulated subscript relative to the full em box size. This is the numerator of the scaling ratio where denominator is the design units per em. If this member is zero, the font does not specify a scale factor, and the client uses its own policy.

### -field superscriptPositionX

Horizontal position of the superscript relative to the baseline origin. This is typically positive (to the right) in italic and oblique fonts, and zero in regular fonts.

### -field superscriptPositionY

Vertical position of the superscript relative to the baseline. This is typically positive.

### -field superscriptSizeX

Horizontal size of the superscript em box in design units, used to scale the simulated superscript relative to the full em box size. This is the numerator of the scaling ratio where denominator is the design units per em. If this member is zero, the font does not specify a scale factor, and the client should use its own policy.

### -field superscriptSizeY

Vertical size of the superscript em box in design units, used to scale the simulated superscript relative to the full em box size. This is the numerator of the scaling ratio where denominator is the design units per em. If this member is zero, the font does not specify a scale factor, and the client should use its own policy.

### -field hasTypographicMetrics

A Boolean value that indicates that the ascent, descent, and lineGap are based on newer 'typographic' values in the font, rather than legacy values.

### -field DWRITE_FONT_METRICS

## -remarks

<b>DWRITE_FONT_METRICS1</b> inherits from <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics">DWRITE_FONT_METRICS</a>:


``` syntax

struct DWRITE_FONT_METRICS1 : public DWRITE_FONT_METRICS
{
...
};
```


## -see-also

<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics">IDWriteFont1::GetMetrics</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getgdicompatiblemetrics">IDWriteFontFace1::GetGdiCompatibleMetrics</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getmetrics">IDWriteFontFace1::GetMetrics</a>

