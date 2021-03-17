---
UID: NE:gdiplusenums.InterpolationMode
title: InterpolationMode (gdiplusenums.h)
description: The InterpolationMode enumeration specifies the algorithm that is used when images are scaled or rotated. This enumeration is used by the Graphics::GetInterpolationMode and Graphics::SetInterpolationMode methods of the Graphics class.
helpviewer_keywords: ["InterpolationMode","InterpolationMode enumeration [GDI+]","InterpolationModeBicubic","InterpolationModeBilinear","InterpolationModeDefault","InterpolationModeHighQuality","InterpolationModeHighQualityBicubic","InterpolationModeHighQualityBilinear","InterpolationModeInvalid","InterpolationModeLowQuality","InterpolationModeNearestNeighbor","_gdiplus_ENUM_InterpolationMode","gdiplus._gdiplus_ENUM_InterpolationMode","gdiplusenums/InterpolationMode","gdiplusenums/InterpolationModeBicubic","gdiplusenums/InterpolationModeBilinear","gdiplusenums/InterpolationModeDefault","gdiplusenums/InterpolationModeHighQuality","gdiplusenums/InterpolationModeHighQualityBicubic","gdiplusenums/InterpolationModeHighQualityBilinear","gdiplusenums/InterpolationModeInvalid","gdiplusenums/InterpolationModeLowQuality","gdiplusenums/InterpolationModeNearestNeighbor"]
old-location: gdiplus\_gdiplus_ENUM_InterpolationMode.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\interpolationmode.htm
ms.date: 12/05/2018
ms.keywords: InterpolationMode, InterpolationMode enumeration [GDI+], InterpolationModeBicubic, InterpolationModeBilinear, InterpolationModeDefault, InterpolationModeHighQuality, InterpolationModeHighQualityBicubic, InterpolationModeHighQualityBilinear, InterpolationModeInvalid, InterpolationModeLowQuality, InterpolationModeNearestNeighbor, _gdiplus_ENUM_InterpolationMode, gdiplus._gdiplus_ENUM_InterpolationMode, gdiplusenums/InterpolationMode, gdiplusenums/InterpolationModeBicubic, gdiplusenums/InterpolationModeBilinear, gdiplusenums/InterpolationModeDefault, gdiplusenums/InterpolationModeHighQuality, gdiplusenums/InterpolationModeHighQualityBicubic, gdiplusenums/InterpolationModeHighQualityBilinear, gdiplusenums/InterpolationModeInvalid, gdiplusenums/InterpolationModeLowQuality, gdiplusenums/InterpolationModeNearestNeighbor
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - InterpolationMode
 - gdiplusenums/InterpolationMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - InterpolationMode
---

# InterpolationMode enumeration


## -description

The <b>InterpolationMode</b> enumeration specifies the algorithm that is used when images are scaled or rotated. This enumeration is used by the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getinterpolationmode">Graphics::GetInterpolationMode</a> and <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode">Graphics::SetInterpolationMode</a> methods of the 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> class.

## -enum-fields

### -field InterpolationModeInvalid

Used internally

### -field InterpolationModeDefault

Specifies the default interpolation mode.

### -field InterpolationModeLowQuality

Specifies a low-quality mode.

### -field InterpolationModeHighQuality

Specifies a high-quality mode.

### -field InterpolationModeBilinear

Specifies bilinear interpolation. No prefiltering is done. This mode is not suitable for shrinking an image below 50 percent of its original size.

### -field InterpolationModeBicubic

Specifies bicubic interpolation. No prefiltering is done. This mode is not suitable for shrinking an image below 25 percent of its original size.

### -field InterpolationModeNearestNeighbor

Specifies nearest-neighbor interpolation.

### -field InterpolationModeHighQualityBilinear

Specifies high-quality, bilinear interpolation. Prefiltering is performed to ensure high-quality shrinking.

### -field InterpolationModeHighQualityBicubic

Specifies high-quality, bicubic interpolation. Prefiltering is performed to ensure high-quality shrinking. This mode produces the highest quality transformed images.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getinterpolationmode">Graphics::GetInterpolationMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode">Graphics::SetInterpolationMode</a>