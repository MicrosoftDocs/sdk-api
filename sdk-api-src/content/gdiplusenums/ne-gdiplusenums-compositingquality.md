---
UID: NE:gdiplusenums.CompositingQuality
title: CompositingQuality (gdiplusenums.h)
description: The CompositingQuality enumeration specifies whether gamma correction is applied when colors are blended with background colors.
helpviewer_keywords: ["CompositingQuality","CompositingQuality enumeration [GDI+]","CompositingQualityAssumeLinear","CompositingQualityDefault","CompositingQualityGammaCorrected","CompositingQualityHighQuality","CompositingQualityHighSpeed","_gdiplus_ENUM_CompositingQuality","gdiplus._gdiplus_ENUM_CompositingQuality","gdiplusenums/CompositingQuality","gdiplusenums/CompositingQualityAssumeLinear","gdiplusenums/CompositingQualityDefault","gdiplusenums/CompositingQualityGammaCorrected","gdiplusenums/CompositingQualityHighQuality","gdiplusenums/CompositingQualityHighSpeed"]
old-location: gdiplus\_gdiplus_ENUM_CompositingQuality.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\compositingquality.htm
ms.date: 12/05/2018
ms.keywords: CompositingQuality, CompositingQuality enumeration [GDI+], CompositingQualityAssumeLinear, CompositingQualityDefault, CompositingQualityGammaCorrected, CompositingQualityHighQuality, CompositingQualityHighSpeed, _gdiplus_ENUM_CompositingQuality, gdiplus._gdiplus_ENUM_CompositingQuality, gdiplusenums/CompositingQuality, gdiplusenums/CompositingQualityAssumeLinear, gdiplusenums/CompositingQualityDefault, gdiplusenums/CompositingQualityGammaCorrected, gdiplusenums/CompositingQualityHighQuality, gdiplusenums/CompositingQualityHighSpeed
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
 - CompositingQuality
 - gdiplusenums/CompositingQuality
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
 - CompositingQuality
---

# CompositingQuality enumeration


## -description

The <b>CompositingQuality</b> enumeration specifies whether gamma correction is applied when colors are blended with background colors. This enumeration is used by the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getcompositingquality">Graphics::GetCompositingQuality</a> and <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality">Graphics::SetCompositingQuality</a> methods of the 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> class.

## -enum-fields

### -field CompositingQualityInvalid

### -field CompositingQualityDefault

Specifies that gamma correction is not applied.

### -field CompositingQualityHighSpeed

Specifies that gamma correction is not applied.

### -field CompositingQualityHighQuality

Specifies that gamma correction is applied.

### -field CompositingQualityGammaCorrected

Specifies that gamma correction is applied.

### -field CompositingQualityAssumeLinear

Specifies that gamma correction is not applied.

## -remarks

When you specify that gamma correction should not be applied, the image data to be rendered (blended with the background) is assumed to be in a linear color space with a gamma value of 1.0. As a result, no gamma adjustment is applied to the image data before or after blending the image with the background.

When you specify that gamma correction should be applied, the image data to be rendered (blended with the background) is assumed to be in the sRGB color space with a gamma value of 2.2. To ensure accurate blending, the input image data is transformed into a linear (gamma = 1.0) space before the colors are blended and transformed back into sRGB (gamma = 2.2) space afterward. This mode results in a more accurate blend at the expense of additional processing time.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getcompositingquality">Graphics::GetCompositingQuality</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality">Graphics::SetCompositingQuality</a>