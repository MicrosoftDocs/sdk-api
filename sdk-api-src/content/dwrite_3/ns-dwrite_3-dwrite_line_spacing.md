---
UID: NS:dwrite_3.DWRITE_LINE_SPACING
title: DWRITE_LINE_SPACING (dwrite_3.h)
description: Sets the vertical spacing between lines of text.
helpviewer_keywords: ["DWRITE_LINE_SPACING","DWRITE_LINE_SPACING structure [Direct Write]","directwrite.dwrite_line_spacing","dwrite_3/DWRITE_LINE_SPACING"]
old-location: directwrite\dwrite_line_spacing.htm
tech.root: DirectWrite
ms.assetid: bb589a7a-374f-52fc-2fa4-4cc72c6ce6dc
ms.date: 12/05/2018
ms.keywords: DWRITE_LINE_SPACING, DWRITE_LINE_SPACING structure [Direct Write], directwrite.dwrite_line_spacing, dwrite_3/DWRITE_LINE_SPACING
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - DWRITE_LINE_SPACING
 - dwrite_3/DWRITE_LINE_SPACING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_3.h
api_name:
 - DWRITE_LINE_SPACING
---

## -description

Sets the vertical spacing between lines of text.

## -struct-fields

### -field method

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method">DWRITE_LINE_SPACING_METHOD</a></b>

Method used to determine line spacing.

### -field height

Type: <b>FLOAT</b>

Spacing between lines. The interpretation of this parameter depends upon the line spacing method, as follows:

<ul>
<li>Line spacing: ignored</li>
<li>uniform line spacing: explicit distance in DIPs between lines</li>
<li>proportional line spacing: a scaling factor to be applied to the computed line height; 
       for each line, the height of the line is computed as for default line spacing, and the scaling factor is applied to that value.</li>
</ul>

### -field baseline

Type: <b>FLOAT</b>

Distance from top of line to baseline. 
       The interpretation of this parameter depends upon the line spacing method, as follows:

<ul>
<li>default line spacing: ignored</li>
<li>uniform line spacing: explicit distance in DIPs from the top of the line to the baseline</li>
<li>proportional line spacing: a scaling factor applied to the computed baseline; for each line, 
       the baseline distance is computed as for default line spacing, and the scaling factor is applied to that value.</li>
</ul>

### -field leadingBefore

Type: <b>FLOAT</b>

Proportion of the entire leading distributed before the line. The allowed value is between 0 and 1.0. The remaining
     leading is distributed after the line. It is ignored for the default and uniform line spacing methods.
     The leading that is available to distribute before or after the line depends on the values of the height and
     baseline parameters.

### -field fontLineGapUsage

Type: <b><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage">DWRITE_FONT_LINE_GAP_USAGE</a></b>

Specify whether <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics">DWRITE_FONT_METRICS</a>::lineGap value should be part of the line metrics.

