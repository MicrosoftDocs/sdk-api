---
UID: NS:dwrite.DWRITE_FONT_METRICS
title: DWRITE_FONT_METRICS (dwrite.h)
description: The DWRITE_FONT_METRICS structure specifies the metrics that are applicable to all glyphs within the font face.
helpviewer_keywords: ["DWRITE_FONT_METRICS","DWRITE_FONT_METRICS structure [Direct Write]","directwrite.dwrite_font_metrics","dwrite/DWRITE_FONT_METRICS"]
old-location: directwrite\dwrite_font_metrics.htm
tech.root: DirectWrite
ms.assetid: ffbf987c-145e-4b93-a48f-8948944c6e33
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_METRICS, DWRITE_FONT_METRICS structure [Direct Write], directwrite.dwrite_font_metrics, dwrite/DWRITE_FONT_METRICS
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - DWRITE_FONT_METRICS
 - dwrite/DWRITE_FONT_METRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_FONT_METRICS
---

# DWRITE_FONT_METRICS structure


## -description

The <b>DWRITE_FONT_METRICS</b> structure specifies the metrics that are applicable to all glyphs within the font face.

## -struct-fields

### -field designUnitsPerEm

Type: <b>UINT16</b>

The number of font design units per em unit. Font files use their own coordinate system of font design units. A font design unit is the smallest measurable unit in the em square, an imaginary square that is used to size and align glyphs. The concept of em square is used as a reference scale factor when defining font size and device transformation semantics. The size of one em square is also commonly used to compute the paragraph indentation value.

### -field ascent

Type: <b>UINT16</b>

The ascent value of the font face in font design units. Ascent is the distance from the top of font character alignment box to the English baseline.

### -field descent

Type: <b>UINT16</b>

The descent value of the font face in font design units. Descent is the distance from the bottom of font character alignment box to the English baseline.

### -field lineGap

Type: <b>INT16</b>

The line gap in font design units. Recommended additional white space to add between lines to improve legibility. The recommended line spacing (baseline-to-baseline distance) is  the sum of <b>ascent</b>, <b>descent</b>, and <b>lineGap</b>. The line gap is usually positive or zero but can be negative, in which case the recommended line spacing is less than the height of the character alignment box.

### -field capHeight

Type: <b>UINT16</b>

The cap height value of the font face in font design units. Cap height is the distance from the English baseline to the top of a typical English capital. Capital "H" is often used as a reference character for the purpose of calculating the cap height value.

### -field xHeight

Type: <b>UINT16</b>

The x-height value of the font face in font design units. x-height is the distance from the English baseline to the top of lowercase letter "x", or a similar lowercase character.

### -field underlinePosition

Type: <b>INT16</b>

The underline position value of the font face in font design units. Underline position is the position of underline relative to the English baseline. The value is usually made negative in order to place the underline below the baseline.

### -field underlineThickness

Type: <b>UINT16</b>

The suggested underline thickness value of the font face in font design units.

### -field strikethroughPosition

Type: <b>INT16</b>

The strikethrough position value of the font face in font design units. Strikethrough position is the position of strikethrough relative to the English baseline. The value is usually made positive in order to place the strikethrough above the baseline.

### -field strikethroughThickness

Type: <b>UINT16</b>

The suggested strikethrough thickness value of the font face in font design units.

