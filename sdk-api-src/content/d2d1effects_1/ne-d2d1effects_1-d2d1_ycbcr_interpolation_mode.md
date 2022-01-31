---
UID: NE:d2d1effects_1.D2D1_YCBCR_INTERPOLATION_MODE
title: D2D1_YCBCR_INTERPOLATION_MODE (d2d1effects_1.h)
description: Specifies the interpolation mode for the YCbCr effect.
helpviewer_keywords: ["D2D1_YCBCR_INTERPOLATION_MODE","D2D1_YCBCR_INTERPOLATION_MODE enumeration [Direct2D]","D2D1_YCBCR_INTERPOLATION_MODE_ANISOTROPIC","D2D1_YCBCR_INTERPOLATION_MODE_CUBIC","D2D1_YCBCR_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC","D2D1_YCBCR_INTERPOLATION_MODE_LINEAR","D2D1_YCBCR_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR","D2D1_YCBCR_INTERPOLATION_MODE_NEAREST_NEIGHBOR","d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE","d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_ANISOTROPIC","d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_CUBIC","d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC","d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_LINEAR","d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR","d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_NEAREST_NEIGHBOR","direct2d.d2d1_ycbcr_interpolation_mode"]
old-location: direct2d\d2d1_ycbcr_interpolation_mode.htm
tech.root: Direct2D
ms.assetid: 30F27963-DF93-46B6-A30E-F89AD634C987
ms.date: 12/05/2018
ms.keywords: D2D1_YCBCR_INTERPOLATION_MODE, D2D1_YCBCR_INTERPOLATION_MODE enumeration [Direct2D], D2D1_YCBCR_INTERPOLATION_MODE_ANISOTROPIC, D2D1_YCBCR_INTERPOLATION_MODE_CUBIC, D2D1_YCBCR_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC, D2D1_YCBCR_INTERPOLATION_MODE_LINEAR, D2D1_YCBCR_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR, D2D1_YCBCR_INTERPOLATION_MODE_NEAREST_NEIGHBOR, d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE, d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_ANISOTROPIC, d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_CUBIC, d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC, d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_LINEAR, d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR, d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE_NEAREST_NEIGHBOR, direct2d.d2d1_ycbcr_interpolation_mode
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
req.typenames: D2D1_YCBCR_INTERPOLATION_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_YCBCR_INTERPOLATION_MODE
 - d2d1effects_1/D2D1_YCBCR_INTERPOLATION_MODE
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
 - D2D1_YCBCR_INTERPOLATION_MODE
---

# D2D1_YCBCR_INTERPOLATION_MODE enumeration


## -description

Specifies the interpolation mode for the <a href="/windows/desktop/Direct2D/ycbcr-effect">YCbCr effect</a>.

## -enum-fields

### -field D2D1_YCBCR_INTERPOLATION_MODE_NEAREST_NEIGHBOR:0

Samples the nearest single point and uses that. This mode uses less processing time, but outputs the lowest quality image.

### -field D2D1_YCBCR_INTERPOLATION_MODE_LINEAR:1

Uses a four point sample and linear interpolation. This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.

### -field D2D1_YCBCR_INTERPOLATION_MODE_CUBIC:2

Uses a 16 sample cubic kernel for interpolation. This mode uses the most processing time, but outputs a higher quality image.

### -field D2D1_YCBCR_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR:3

Uses 4 linear samples within a single pixel for good edge anti-aliasing. This mode is good for scaling down by small amounts on images with few pixels.

### -field D2D1_YCBCR_INTERPOLATION_MODE_ANISOTROPIC:4

Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.

### -field D2D1_YCBCR_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC:5

Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix. Then uses the cubic interpolation mode for the final output.

### -field D2D1_YCBCR_INTERPOLATION_MODE_FORCE_DWORD:0xffffffff
