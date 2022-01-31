---
UID: NE:gdiplusimaging.ImageFlags
title: ImageFlags (gdiplusimaging.h)
description: The ImageFlags enumeration specifies the attributes of the pixel data contained in an Image object. The Image::GetFlags method returns an element of this enumeration.
helpviewer_keywords: ["ImageFlags","ImageFlags enumeration [GDI+]","ImageFlagsCaching","ImageFlagsColorSpaceCMYK","ImageFlagsColorSpaceGRAY","ImageFlagsColorSpaceRGB","ImageFlagsColorSpaceYCBCR","ImageFlagsColorSpaceYCCK","ImageFlagsHasAlpha","ImageFlagsHasRealDPI","ImageFlagsHasRealPixelSize","ImageFlagsHasTranslucent","ImageFlagsNone","ImageFlagsPartiallyScalable","ImageFlagsReadOnly","ImageFlagsScalable","_gdiplus_ENUM_ImageFlags","gdiplus._gdiplus_ENUM_ImageFlags","gdiplusimaging/ImageFlags","gdiplusimaging/ImageFlagsCaching","gdiplusimaging/ImageFlagsColorSpaceCMYK","gdiplusimaging/ImageFlagsColorSpaceGRAY","gdiplusimaging/ImageFlagsColorSpaceRGB","gdiplusimaging/ImageFlagsColorSpaceYCBCR","gdiplusimaging/ImageFlagsColorSpaceYCCK","gdiplusimaging/ImageFlagsHasAlpha","gdiplusimaging/ImageFlagsHasRealDPI","gdiplusimaging/ImageFlagsHasRealPixelSize","gdiplusimaging/ImageFlagsHasTranslucent","gdiplusimaging/ImageFlagsNone","gdiplusimaging/ImageFlagsPartiallyScalable","gdiplusimaging/ImageFlagsReadOnly","gdiplusimaging/ImageFlagsScalable"]
old-location: gdiplus\_gdiplus_ENUM_ImageFlags.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\imageflags.htm
ms.date: 12/05/2018
ms.keywords: ImageFlags, ImageFlags enumeration [GDI+], ImageFlagsCaching, ImageFlagsColorSpaceCMYK, ImageFlagsColorSpaceGRAY, ImageFlagsColorSpaceRGB, ImageFlagsColorSpaceYCBCR, ImageFlagsColorSpaceYCCK, ImageFlagsHasAlpha, ImageFlagsHasRealDPI, ImageFlagsHasRealPixelSize, ImageFlagsHasTranslucent, ImageFlagsNone, ImageFlagsPartiallyScalable, ImageFlagsReadOnly, ImageFlagsScalable, _gdiplus_ENUM_ImageFlags, gdiplus._gdiplus_ENUM_ImageFlags, gdiplusimaging/ImageFlags, gdiplusimaging/ImageFlagsCaching, gdiplusimaging/ImageFlagsColorSpaceCMYK, gdiplusimaging/ImageFlagsColorSpaceGRAY, gdiplusimaging/ImageFlagsColorSpaceRGB, gdiplusimaging/ImageFlagsColorSpaceYCBCR, gdiplusimaging/ImageFlagsColorSpaceYCCK, gdiplusimaging/ImageFlagsHasAlpha, gdiplusimaging/ImageFlagsHasRealDPI, gdiplusimaging/ImageFlagsHasRealPixelSize, gdiplusimaging/ImageFlagsHasTranslucent, gdiplusimaging/ImageFlagsNone, gdiplusimaging/ImageFlagsPartiallyScalable, gdiplusimaging/ImageFlagsReadOnly, gdiplusimaging/ImageFlagsScalable
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - ImageFlags
 - gdiplusimaging/ImageFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusimaging.h
api_name:
 - ImageFlags
---

# ImageFlags enumeration


## -description

The <b>ImageFlags</b> enumeration specifies the attributes of the pixel data contained in an 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object. The 
			<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getflags">Image::GetFlags</a> method returns an element of this enumeration.

## -enum-fields

### -field ImageFlagsNone:0

Specifies no format information.

### -field ImageFlagsScalable:0x0001

Specifies that the image can be scaled.

### -field ImageFlagsHasAlpha:0x0002

Specifies that the pixel data contains alpha values.

### -field ImageFlagsHasTranslucent:0x0004

Specifies that the pixel data has alpha values other than 0 (transparent) and 255 (opaque).

### -field ImageFlagsPartiallyScalable:0x0008

Specifies that the pixel data is partially scalable with some limitations.

### -field ImageFlagsColorSpaceRGB:0x0010

Specifies that the image is stored using an RGB color space.

### -field ImageFlagsColorSpaceCMYK:0x0020

Specifies that the image is stored using a CMYK color space.

### -field ImageFlagsColorSpaceGRAY:0x0040

Specifies that the image is a grayscale image.

### -field ImageFlagsColorSpaceYCBCR:0x0080

Specifies that the image is stored using a YCBCR color space.

### -field ImageFlagsColorSpaceYCCK:0x0100

Specifies that the image is stored using a YCCK color space.

### -field ImageFlagsHasRealDPI:0x1000

Specifies that dots per inch information is stored in the image.

### -field ImageFlagsHasRealPixelSize:0x2000

Specifies that the pixel size is stored in the image.

### -field ImageFlagsReadOnly:0x00010000

Specifies that the pixel data is read-only.

### -field ImageFlagsCaching:0x00020000

Specifies that the pixel data can be cached for faster access.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getflags">Image::GetFlags</a>
