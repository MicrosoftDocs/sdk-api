---
UID: NE:d2d1_1.D2D1_INTERPOLATION_MODE
title: D2D1_INTERPOLATION_MODE (d2d1_1.h)
description: This is used to specify the quality of image scaling with ID2D1DeviceContext::DrawImage and with the 2D affine transform effect.
helpviewer_keywords: ["D2D1_INTERPOLATION_MODE","D2D1_INTERPOLATION_MODE enumeration [Direct2D]","D2D1_INTERPOLATION_MODE_ANISOTROPIC","D2D1_INTERPOLATION_MODE_CUBIC","D2D1_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC","D2D1_INTERPOLATION_MODE_LINEAR","D2D1_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR","D2D1_INTERPOLATION_MODE_NEAREST_NEIGHBOR","d2d1_1/D2D1_INTERPOLATION_MODE","d2d1_1/D2D1_INTERPOLATION_MODE_ANISOTROPIC","d2d1_1/D2D1_INTERPOLATION_MODE_CUBIC","d2d1_1/D2D1_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC","d2d1_1/D2D1_INTERPOLATION_MODE_LINEAR","d2d1_1/D2D1_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR","d2d1_1/D2D1_INTERPOLATION_MODE_NEAREST_NEIGHBOR","direct2d.__D2D1_INTERPOLATION_MODE","direct2d.__d2d1_image_interpolation_mode"]
old-location: direct2d\__d2d1_image_interpolation_mode.htm
tech.root: Direct2D
ms.assetid: 7a32f551-afad-4eb2-953f-a9acc71d7776
ms.date: 12/05/2018
ms.keywords: D2D1_INTERPOLATION_MODE, D2D1_INTERPOLATION_MODE enumeration [Direct2D], D2D1_INTERPOLATION_MODE_ANISOTROPIC, D2D1_INTERPOLATION_MODE_CUBIC, D2D1_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC, D2D1_INTERPOLATION_MODE_LINEAR, D2D1_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR, D2D1_INTERPOLATION_MODE_NEAREST_NEIGHBOR, d2d1_1/D2D1_INTERPOLATION_MODE, d2d1_1/D2D1_INTERPOLATION_MODE_ANISOTROPIC, d2d1_1/D2D1_INTERPOLATION_MODE_CUBIC, d2d1_1/D2D1_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC, d2d1_1/D2D1_INTERPOLATION_MODE_LINEAR, d2d1_1/D2D1_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR, d2d1_1/D2D1_INTERPOLATION_MODE_NEAREST_NEIGHBOR, direct2d.__D2D1_INTERPOLATION_MODE, direct2d.__d2d1_image_interpolation_mode
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D2D1_INTERPOLATION_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_INTERPOLATION_MODE
 - d2d1_1/D2D1_INTERPOLATION_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2d1_1.h
api_name:
 - D2D1_INTERPOLATION_MODE
---

# D2D1_INTERPOLATION_MODE enumeration


## -description

This is used to specify the quality of image scaling with  <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a> and with the <a href="/windows/desktop/Direct2D/2d-affine-transform">2D affine transform effect</a>.

## -enum-fields

### -field D2D1_INTERPOLATION_MODE_NEAREST_NEIGHBOR

Samples the nearest single point and uses that exact color.  This mode uses less processing time, but outputs the lowest quality image.

### -field D2D1_INTERPOLATION_MODE_LINEAR

Uses a four point sample and linear interpolation. This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.

### -field D2D1_INTERPOLATION_MODE_CUBIC

Uses a 16 sample cubic kernel for interpolation.  This mode uses the most processing time, but outputs a higher quality image.

### -field D2D1_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR

Uses 4 linear samples within a single pixel for good edge anti-aliasing. This mode is good for scaling down by small amounts on images with few pixels.

### -field D2D1_INTERPOLATION_MODE_ANISOTROPIC

Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.

### -field D2D1_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC

Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix. Then uses the cubic interpolation mode for the final output.

### -field D2D1_INTERPOLATION_MODE_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a>
