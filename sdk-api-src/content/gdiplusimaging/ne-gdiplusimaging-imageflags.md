---
UID: NE:gdiplusimaging.ImageFlags
title: ImageFlags (gdiplusimaging.h)

description: The ImageFlags enumeration specifies the attributes of the pixel data contained in an Image object. The Image::GetFlags method returns an element of this enumeration.
old-location: gdiplus\_gdiplus_ENUM_ImageFlags.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\imageflags.htm

ms.date: 12/05/2018
ms.keywords: ImageFlags, ImageFlags enumeration [GDI+], ImageFlagsCaching, ImageFlagsColorSpaceCMYK, ImageFlagsColorSpaceGRAY, ImageFlagsColorSpaceRGB, ImageFlagsColorSpaceYCBCR, ImageFlagsColorSpaceYCCK, ImageFlagsHasAlpha, ImageFlagsHasRealDPI, ImageFlagsHasRealPixelSize, ImageFlagsHasTranslucent, ImageFlagsNone, ImageFlagsPartiallyScalable, ImageFlagsReadOnly, ImageFlagsScalable, _gdiplus_ENUM_ImageFlags, gdiplus._gdiplus_ENUM_ImageFlags, gdiplusimaging/ImageFlags, gdiplusimaging/ImageFlagsCaching, gdiplusimaging/ImageFlagsColorSpaceCMYK, gdiplusimaging/ImageFlagsColorSpaceGRAY, gdiplusimaging/ImageFlagsColorSpaceRGB, gdiplusimaging/ImageFlagsColorSpaceYCBCR, gdiplusimaging/ImageFlagsColorSpaceYCCK, gdiplusimaging/ImageFlagsHasAlpha, gdiplusimaging/ImageFlagsHasRealDPI, gdiplusimaging/ImageFlagsHasRealPixelSize, gdiplusimaging/ImageFlagsHasTranslucent, gdiplusimaging/ImageFlagsNone, gdiplusimaging/ImageFlagsPartiallyScalable, gdiplusimaging/ImageFlagsReadOnly, gdiplusimaging/ImageFlagsScalable
ms.topic: enum
f1_keywords: 
 - "gdiplusimaging/ImageFlags"
dev_langs:
 - c++
req.header: gdiplusimaging.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusimaging.h
api_name:
 - ImageFlags
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# ImageFlags enumeration


## -description


The <b>ImageFlags</b> enumeration specifies the attributes of the pixel data contained in an 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object. The 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getflags">Image::GetFlags</a> method returns an element of this enumeration.


## -enum-fields




### -field ImageFlagsNone

Specifies no format information. 


### -field ImageFlagsScalable

Specifies that the image can be scaled. 


### -field ImageFlagsHasAlpha

Specifies that the pixel data contains alpha values. 


### -field ImageFlagsHasTranslucent

Specifies that the pixel data has alpha values other than 0 (transparent) and 255 (opaque). 


### -field ImageFlagsPartiallyScalable

Specifies that the pixel data is partially scalable with some limitations. 


### -field ImageFlagsColorSpaceRGB

Specifies that the image is stored using an RGB color space. 


### -field ImageFlagsColorSpaceCMYK

Specifies that the image is stored using a CMYK color space. 


### -field ImageFlagsColorSpaceGRAY

Specifies that the image is a grayscale image. 


### -field ImageFlagsColorSpaceYCBCR

Specifies that the image is stored using a YCBCR color space. 


### -field ImageFlagsColorSpaceYCCK

Specifies that the image is stored using a YCCK color space. 


### -field ImageFlagsHasRealDPI

Specifies that dots per inch information is stored in the image. 


### -field ImageFlagsHasRealPixelSize

Specifies that the pixel size is stored in the image. 


### -field ImageFlagsReadOnly

Specifies that the pixel data is read-only. 


### -field ImageFlagsCaching

Specifies that the pixel data can be cached for faster access. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getflags">Image::GetFlags</a>
 

 

