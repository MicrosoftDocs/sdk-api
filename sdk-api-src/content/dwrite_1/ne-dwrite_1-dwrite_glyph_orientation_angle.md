---
UID: NE:dwrite_1.DWRITE_GLYPH_ORIENTATION_ANGLE
title: DWRITE_GLYPH_ORIENTATION_ANGLE (dwrite_1.h)
description: The DWRITE_GLYPH_ORIENTATION_ANGLE enumeration contains values that specify how the glyph is oriented to the x-axis.
helpviewer_keywords: ["DWRITE_GLYPH_ORIENTATION_ANGLE","DWRITE_GLYPH_ORIENTATION_ANGLE enumeration [Direct Write]","DWRITE_GLYPH_ORIENTATION_ANGLE_0_DEGREES","DWRITE_GLYPH_ORIENTATION_ANGLE_180_DEGREES","DWRITE_GLYPH_ORIENTATION_ANGLE_270_DEGREES","DWRITE_GLYPH_ORIENTATION_ANGLE_90_DEGREES","directwrite.dwrite_glyph_orientation_angle","dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE","dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE_0_DEGREES","dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE_180_DEGREES","dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE_270_DEGREES","dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE_90_DEGREES"]
old-location: directwrite\dwrite_glyph_orientation_angle.htm
tech.root: DirectWrite
ms.assetid: BD9D0C11-B286-4E4A-B641-1DB9F75803B0
ms.date: 12/05/2018
ms.keywords: DWRITE_GLYPH_ORIENTATION_ANGLE, DWRITE_GLYPH_ORIENTATION_ANGLE enumeration [Direct Write], DWRITE_GLYPH_ORIENTATION_ANGLE_0_DEGREES, DWRITE_GLYPH_ORIENTATION_ANGLE_180_DEGREES, DWRITE_GLYPH_ORIENTATION_ANGLE_270_DEGREES, DWRITE_GLYPH_ORIENTATION_ANGLE_90_DEGREES, directwrite.dwrite_glyph_orientation_angle, dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE, dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE_0_DEGREES, dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE_180_DEGREES, dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE_270_DEGREES, dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE_90_DEGREES
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
 - DWRITE_GLYPH_ORIENTATION_ANGLE
 - dwrite_1/DWRITE_GLYPH_ORIENTATION_ANGLE
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
 - DWRITE_GLYPH_ORIENTATION_ANGLE
---

# DWRITE_GLYPH_ORIENTATION_ANGLE enumeration


## -description

The <b>DWRITE_GLYPH_ORIENTATION_ANGLE</b> enumeration contains values that specify how the glyph is oriented to the x-axis.

## -enum-fields

### -field DWRITE_GLYPH_ORIENTATION_ANGLE_0_DEGREES

Glyph orientation is upright.

### -field DWRITE_GLYPH_ORIENTATION_ANGLE_90_DEGREES

Glyph orientation is rotated 90 degrees clockwise.

### -field DWRITE_GLYPH_ORIENTATION_ANGLE_180_DEGREES

Glyph orientation is upside-down.

### -field DWRITE_GLYPH_ORIENTATION_ANGLE_270_DEGREES

Glyph orientation is rotated 270 degrees clockwise.

## -remarks

The text analyzer outputs <b>DWRITE_GLYPH_ORIENTATION_ANGLE</b> values. The value that it outputs depends on the desired orientation, bidi level, and character properties.

## -see-also

<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalysissink1-setglyphorientation">IDWriteTextAnalysisSink1::SetGlyphOrientation</a>



<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform">IDWriteTextAnalyzer1::GetGlyphOrientationTransform</a>

