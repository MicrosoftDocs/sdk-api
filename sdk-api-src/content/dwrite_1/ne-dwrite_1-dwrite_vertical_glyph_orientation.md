---
UID: NE:dwrite_1.DWRITE_VERTICAL_GLYPH_ORIENTATION
title: DWRITE_VERTICAL_GLYPH_ORIENTATION (dwrite_1.h)
description: The DWRITE_VERTICAL_GLYPH_ORIENTATION enumeration contains values that specify the desired kind of glyph orientation for the text.
helpviewer_keywords: ["DWRITE_VERTICAL_GLYPH_ORIENTATION","DWRITE_VERTICAL_GLYPH_ORIENTATION enumeration [Direct Write]","DWRITE_VERTICAL_GLYPH_ORIENTATION_DEFAULT","DWRITE_VERTICAL_GLYPH_ORIENTATION_STACKED","directwrite.dwrite_vertical_glyph_orientation","dwrite_1/DWRITE_VERTICAL_GLYPH_ORIENTATION","dwrite_1/DWRITE_VERTICAL_GLYPH_ORIENTATION_DEFAULT","dwrite_1/DWRITE_VERTICAL_GLYPH_ORIENTATION_STACKED"]
old-location: directwrite\dwrite_vertical_glyph_orientation.htm
tech.root: DirectWrite
ms.assetid: F13CD254-0D6A-4549-A2C2-3D3126E7B2EB
ms.date: 12/05/2018
ms.keywords: DWRITE_VERTICAL_GLYPH_ORIENTATION, DWRITE_VERTICAL_GLYPH_ORIENTATION enumeration [Direct Write], DWRITE_VERTICAL_GLYPH_ORIENTATION_DEFAULT, DWRITE_VERTICAL_GLYPH_ORIENTATION_STACKED, directwrite.dwrite_vertical_glyph_orientation, dwrite_1/DWRITE_VERTICAL_GLYPH_ORIENTATION, dwrite_1/DWRITE_VERTICAL_GLYPH_ORIENTATION_DEFAULT, dwrite_1/DWRITE_VERTICAL_GLYPH_ORIENTATION_STACKED
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
 - DWRITE_VERTICAL_GLYPH_ORIENTATION
 - dwrite_1/DWRITE_VERTICAL_GLYPH_ORIENTATION
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
 - DWRITE_VERTICAL_GLYPH_ORIENTATION
---

# DWRITE_VERTICAL_GLYPH_ORIENTATION enumeration


## -description

The <b>DWRITE_VERTICAL_GLYPH_ORIENTATION</b> enumeration contains values that specify the desired kind of glyph orientation for the text.

## -enum-fields

### -field DWRITE_VERTICAL_GLYPH_ORIENTATION_DEFAULT

The default glyph orientation. In vertical layout, naturally horizontal scripts (Latin, Thai, Arabic, Devanagari) rotate 90 degrees clockwise, while ideographic scripts (Chinese, Japanese, Korean) remain upright, 0 degrees.

### -field DWRITE_VERTICAL_GLYPH_ORIENTATION_STACKED

Stacked glyph orientation. Ideographic scripts and scripts that permit stacking (Latin, Hebrew) are stacked in vertical reading layout. Connected scripts (Arabic, Syriac, 'Phags-pa, Ogham), which would otherwise look broken if glyphs were kept at 0 degrees, remain connected and rotate.

## -remarks

The client specifies a <b>DWRITE_VERTICAL_GLYPH_ORIENTATION</b>-typed value to the analyzer as the desired orientation.

<div class="alert"><b>Note</b>  This is the client preference, and the constraints of the script determine the final presentation.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalysissource1-getverticalglyphorientation">IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation</a>

