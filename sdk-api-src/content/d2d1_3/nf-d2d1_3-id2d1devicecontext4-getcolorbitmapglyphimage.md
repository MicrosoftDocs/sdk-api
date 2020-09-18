---
UID: NF:d2d1_3.ID2D1DeviceContext4.GetColorBitmapGlyphImage
title: ID2D1DeviceContext4::GetColorBitmapGlyphImage (d2d1_3.h)
description: Retrieves an image of the color bitmap glyph from the color glyph cache.
helpviewer_keywords: ["GetColorBitmapGlyphImage","GetColorBitmapGlyphImage method [Direct2D]","GetColorBitmapGlyphImage method [Direct2D]","ID2D1DeviceContext4 interface","ID2D1DeviceContext4 interface [Direct2D]","GetColorBitmapGlyphImage method","ID2D1DeviceContext4.GetColorBitmapGlyphImage","ID2D1DeviceContext4::GetColorBitmapGlyphImage","d2d1_3/ID2D1DeviceContext4::GetColorBitmapGlyphImage","direct2d.id2d1devicecontext4_getcolorbitmapglyphimage"]
old-location: direct2d\id2d1devicecontext4_getcolorbitmapglyphimage.htm
tech.root: Direct2D
ms.assetid: 493224CD-A31E-405B-A084-24C377F713A0
ms.date: 12/05/2018
ms.keywords: GetColorBitmapGlyphImage, GetColorBitmapGlyphImage method [Direct2D], GetColorBitmapGlyphImage method [Direct2D],ID2D1DeviceContext4 interface, ID2D1DeviceContext4 interface [Direct2D],GetColorBitmapGlyphImage method, ID2D1DeviceContext4.GetColorBitmapGlyphImage, ID2D1DeviceContext4::GetColorBitmapGlyphImage, d2d1_3/ID2D1DeviceContext4::GetColorBitmapGlyphImage, direct2d.id2d1devicecontext4_getcolorbitmapglyphimage
req.header: d2d1_3.h
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext4::GetColorBitmapGlyphImage
 - d2d1_3/ID2D1DeviceContext4::GetColorBitmapGlyphImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext4.GetColorBitmapGlyphImage
---

# ID2D1DeviceContext4::GetColorBitmapGlyphImage


## -description

Retrieves an image of the color bitmap glyph from the color glyph cache. If the
          cache does not already contain the requested resource, it will be created. This
          method may be used to extend the lifetime of a glyph image even after it is
          evicted from the color glyph cache.

## -parameters

### -param glyphImageFormat

Type: <b><a href="/windows/desktop/api/dcommon/ne-dcommon-dwrite_glyph_image_formats">DWRITE_GLYPH_IMAGE_FORMATS</a></b>

The format for the glyph image.
          If there is no image data in the requested format for the requested glyph, this method will return an error.

### -param glyphOrigin

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The origin for the glyph.

### -param fontFace [in]

Type: <b><a href="/windows/desktop/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>*</b>

Reference to a font face which contains font face type, appropriate file references, face identification data and various font data such as metrics, names and glyph outlines.

### -param fontEmSize

Type: <b>FLOAT</b>

The specified font size affects the choice of which bitmap to use from the font. It also affects the output glyphTransform, causing  it to properly scale the glyph.

### -param glyphIndex

Type: <b>UINT16</b>

Index of the glyph.

### -param isSideways

Type: <b>BOOL</b>

If true, specifies that glyphs are rotated 90 degrees to the left and vertical metrics are used. Vertical writing is achieved by specifying isSideways as true and rotating the entire run 90 degrees to the right via a rotate transform.

### -param worldTransform [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the image. This input transform affects the choice of which bitmap to use from the font. It is also factored into the output glyphTransform.

### -param dpiX

Type: <b>FLOAT</b>

Dots per inch along the x-axis.

### -param dpiY

Type: <b>FLOAT</b>

Dots per inch along the y-axis.

### -param glyphTransform [out]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

Output transform, which transforms from the glyph's space to the same output space as the worldTransform. This includes the input
          glyphOrigin, the glyph's offset from the glyphOrigin, and any other required transformations.

### -param glyphImage [out]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>**</b>

On completion contains the retrieved glyph image.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext4">ID2D1DeviceContext4</a>