---
UID: NF:dwrite_3.IDWriteFontFace4.GetGlyphImageData
title: IDWriteFontFace4::GetGlyphImageData (dwrite_3.h)
description: Gets a pointer to the glyph data based on the desired image format.
helpviewer_keywords: ["GetGlyphImageData","GetGlyphImageData method [Direct Write]","GetGlyphImageData method [Direct Write]","IDWriteFontFace4 interface","IDWriteFontFace4 interface [Direct Write]","GetGlyphImageData method","IDWriteFontFace4.GetGlyphImageData","IDWriteFontFace4::GetGlyphImageData","directwrite.idwritefontface4_getglyphimagedata","dwrite_3/IDWriteFontFace4::GetGlyphImageData"]
old-location: directwrite\idwritefontface4_getglyphimagedata.htm
tech.root: DirectWrite
ms.assetid: 2517A029-5ACF-4CB2-8A20-98253946DF5E
ms.date: 09/10/2025
ms.keywords: GetGlyphImageData, GetGlyphImageData method [Direct Write], GetGlyphImageData method [Direct Write],IDWriteFontFace4 interface, IDWriteFontFace4 interface [Direct Write],GetGlyphImageData method, IDWriteFontFace4.GetGlyphImageData, IDWriteFontFace4::GetGlyphImageData, directwrite.idwritefontface4_getglyphimagedata, dwrite_3/IDWriteFontFace4::GetGlyphImageData
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 14393
req.target-min-winversvr: Windows 10 Build 14393
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFace4::GetGlyphImageData
 - dwrite_3/IDWriteFontFace4::GetGlyphImageData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontFace4.GetGlyphImageData
---

# IDWriteFontFace4::GetGlyphImageData


## -description

Gets a pointer to the glyph data based on the desired image format.

## -parameters

### -param glyphId [in]

Type: <b>UINT16</b>

The ID of the glyph to retrieve image data for.

### -param pixelsPerEm

Type: <b>UINT32</b>

Requested pixels per em.

### -param glyphImageFormat

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats">DWRITE_GLYPH_IMAGE_FORMATS</a></b>

Specifies which formats are supported in the font.

### -param glyphData [out]

Type: <b><a href="/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data">DWRITE_GLYPH_IMAGE_DATA</a>*</b>

On return contains data for a glyph.

### -param glyphDataContext [out]

Type: <b>void**</b>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

The glyphDataContext must be released via <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontface4-releaseglyphimagedata">ReleaseGlyphImageData</a> when done if the data is not empty,
     similar to <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment">IDWriteFontFileStream::ReadFileFragment</a> 
       and <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-releasefilefragment">IDWriteFontFileStream::ReleaseFileFragment</a>.
     The data pointer is valid so long as the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a> exists and <b>ReleaseGlyphImageData</b> has not
     been called.
     

The <a href="/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data">DWRITE_GLYPH_IMAGE_DATA::uniqueDataId</a> is valuable for caching purposes so that if the same
     resource is returned more than once, an existing resource can be quickly retrieved rather than
     needing to reparse or decompress the data.
     

The function only returns SVG or raster data - requesting TrueType/CFF/COLR data returns
     DWRITE_E_INVALIDARG. Those must be drawn via DrawGlyphRun or queried using GetGlyphOutline instead.
     Exactly one format may be requested or else the function returns DWRITE_E_INVALIDARG.
     If the glyph does not have that format, the call is not an error, but the function returns empty data.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4">IDWriteFontFace4</a>

