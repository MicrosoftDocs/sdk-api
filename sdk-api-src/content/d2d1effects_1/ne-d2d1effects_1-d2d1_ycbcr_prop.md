---
UID: NE:d2d1effects_1.D2D1_YCBCR_PROP
title: D2D1_YCBCR_PROP (d2d1effects_1.h)
description: Identifiers for properties of the YCbCr effect.
helpviewer_keywords: ["D2D1_YCBCR_PROP","D2D1_YCBCR_PROP enumeration [Direct2D]","D2D1_YCBCR_PROP_CHROMA_SUBSAMPLING","D2D1_YCBCR_PROP_INTERPOLATION_MODE","D2D1_YCBCR_PROP_TRANSFORM_MATRIX","d2d1effects_1/D2D1_YCBCR_PROP","d2d1effects_1/D2D1_YCBCR_PROP_CHROMA_SUBSAMPLING","d2d1effects_1/D2D1_YCBCR_PROP_INTERPOLATION_MODE","d2d1effects_1/D2D1_YCBCR_PROP_TRANSFORM_MATRIX","direct2d.d2d1_ycbcr_prop"]
old-location: direct2d\d2d1_ycbcr_prop.htm
tech.root: Direct2D
ms.assetid: 08019B09-0254-48B3-9213-3E7362358109
ms.date: 12/05/2018
ms.keywords: D2D1_YCBCR_PROP, D2D1_YCBCR_PROP enumeration [Direct2D], D2D1_YCBCR_PROP_CHROMA_SUBSAMPLING, D2D1_YCBCR_PROP_INTERPOLATION_MODE, D2D1_YCBCR_PROP_TRANSFORM_MATRIX, d2d1effects_1/D2D1_YCBCR_PROP, d2d1effects_1/D2D1_YCBCR_PROP_CHROMA_SUBSAMPLING, d2d1effects_1/D2D1_YCBCR_PROP_INTERPOLATION_MODE, d2d1effects_1/D2D1_YCBCR_PROP_TRANSFORM_MATRIX, direct2d.d2d1_ycbcr_prop
req.header: d2d1effects_1.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D2D1_YCBCR_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_YCBCR_PROP
 - d2d1effects_1/D2D1_YCBCR_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_1.h
api_name:
 - D2D1_YCBCR_PROP
---

# D2D1_YCBCR_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/ycbcr-effect">YCbCr effect</a>.

## -enum-fields

### -field D2D1_YCBCR_PROP_CHROMA_SUBSAMPLING:0

Specifies the chroma subsampling of the input chroma image.
            

The type is <a href="/windows/desktop/api/d2d1effects_1/ne-d2d1effects_1-d2d1_ycbcr_chroma_subsampling">D2D1_YCBCR_CHROMA_SUBSAMPLING</a>.

The default value is D2D1_YCBCR_CHROMA_SUBSAMPLING_AUTO.

### -field D2D1_YCBCR_PROP_TRANSFORM_MATRIX:1

A 3x2 Matrix specifying the axis-aligned affine transform of the image. Axis aligned transforms include Scale, Flips, and 90 degree rotations.
            

The type is <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>.

The default value is Matrix3x2F::Identity().

### -field D2D1_YCBCR_PROP_INTERPOLATION_MODE:2

The interpolation mode.
            

The type is <a href="/windows/desktop/api/d2d1effects_1/ne-d2d1effects_1-d2d1_ycbcr_interpolation_mode">D2D1_YCBCR_INTERPOLATION_MODE</a>.

### -field D2D1_YCBCR_PROP_FORCE_DWORD:0xffffffff
