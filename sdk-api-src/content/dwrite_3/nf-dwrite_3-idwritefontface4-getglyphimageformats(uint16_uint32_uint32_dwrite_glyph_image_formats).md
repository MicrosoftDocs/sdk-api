---
UID: NF:dwrite_3.IDWriteFontFace4.GetGlyphImageFormats(UINT16,UINT32,UINT32,DWRITE_GLYPH_IMAGE_FORMATS)
title: IDWriteFontFace4::GetGlyphImageFormats(UINT16,UINT32,UINT32,DWRITE_GLYPH_IMAGE_FORMATS) (dwrite_3.h)
description: Gets all the glyph image formats supported by the entire font. (overload 1/2)
helpviewer_keywords: ["GetGlyphImageFormats","GetGlyphImageFormats method [Direct Write]","GetGlyphImageFormats method [Direct Write]","IDWriteFontFace4 interface","IDWriteFontFace4 interface [Direct Write]","GetGlyphImageFormats method","IDWriteFontFace4.GetGlyphImageFormats","IDWriteFontFace4.GetGlyphImageFormats(UINT16","UINT32","UINT32","DWRITE_GLYPH_IMAGE_FORMATS)","IDWriteFontFace4::GetGlyphImageFormats","IDWriteFontFace4::GetGlyphImageFormats(UINT16","UINT32","UINT32","DWRITE_GLYPH_IMAGE_FORMATS)","directwrite.idwritefontface4_getglyphimageformats","dwrite_3/IDWriteFontFace4::GetGlyphImageFormats"]
old-location: directwrite\idwritefontface4_getglyphimageformats.htm
tech.root: DirectWrite
ms.assetid: BE3AC023-48A5-4687-A41D-39C4DF3B853F
ms.date: 09/10/2025
ms.keywords: GetGlyphImageFormats, GetGlyphImageFormats method [Direct Write], GetGlyphImageFormats method [Direct Write],IDWriteFontFace4 interface, IDWriteFontFace4 interface [Direct Write],GetGlyphImageFormats method, IDWriteFontFace4.GetGlyphImageFormats, IDWriteFontFace4.GetGlyphImageFormats(UINT16,UINT32,UINT32,DWRITE_GLYPH_IMAGE_FORMATS), IDWriteFontFace4::GetGlyphImageFormats, IDWriteFontFace4::GetGlyphImageFormats(UINT16,UINT32,UINT32,DWRITE_GLYPH_IMAGE_FORMATS), directwrite.idwritefontface4_getglyphimageformats, dwrite_3/IDWriteFontFace4::GetGlyphImageFormats
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
 - IDWriteFontFace4::GetGlyphImageFormats
 - dwrite_3/IDWriteFontFace4::GetGlyphImageFormats
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
 - IDWriteFontFace4.GetGlyphImageFormats
---

# IDWriteFontFace4::GetGlyphImageFormats(UINT16,UINT32,UINT32,DWRITE_GLYPH_IMAGE_FORMATS)


## -description

Gets all the glyph image formats supported for the specified glyph.

## -parameters

### -param glyphId

The identifier of the glyph to be queried.

### -param pixelsPerEmFirst

The lowest pixels per em value to query.

### -param pixelsPerEmLast

The highest pixels per em value to query.

### -param glyphImageFormats

An array of <a href="/windows/desktop/api/dcommon/ne-dcommon-dwrite_glyph_image_formats">DWRITE_GLYPH_IMAGE_FORMATS</a> specifying the supported formats for the requested glyph.

## -returns

HRESULT

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats">DWRITE_GLYPH_IMAGE_FORMATS</a></b>

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4">IDWriteFontFace4</a>
