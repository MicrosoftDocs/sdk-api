---
UID: NF:dwrite.IDWriteGlyphRunAnalysis.CreateAlphaTexture
title: IDWriteGlyphRunAnalysis::CreateAlphaTexture (dwrite.h)
description: Creates an alpha texture of the specified type for glyphs within a specified bounding rectangle.
helpviewer_keywords: ["CreateAlphaTexture","CreateAlphaTexture method [Direct Write]","CreateAlphaTexture method [Direct Write]","IDWriteGlyphRunAnalysis interface","IDWriteGlyphRunAnalysis interface [Direct Write]","CreateAlphaTexture method","IDWriteGlyphRunAnalysis.CreateAlphaTexture","IDWriteGlyphRunAnalysis::CreateAlphaTexture","directwrite.IDWriteGlyphRunAnalysis_CreateAlphaTexture","dwrite/IDWriteGlyphRunAnalysis::CreateAlphaTexture"]
old-location: directwrite\IDWriteGlyphRunAnalysis_CreateAlphaTexture.htm
tech.root: DirectWrite
ms.assetid: a3a28efa-b235-4608-8410-15cc0ebfe38e
ms.date: 12/05/2018
ms.keywords: CreateAlphaTexture, CreateAlphaTexture method [Direct Write], CreateAlphaTexture method [Direct Write],IDWriteGlyphRunAnalysis interface, IDWriteGlyphRunAnalysis interface [Direct Write],CreateAlphaTexture method, IDWriteGlyphRunAnalysis.CreateAlphaTexture, IDWriteGlyphRunAnalysis::CreateAlphaTexture, directwrite.IDWriteGlyphRunAnalysis_CreateAlphaTexture, dwrite/IDWriteGlyphRunAnalysis::CreateAlphaTexture
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteGlyphRunAnalysis::CreateAlphaTexture
 - dwrite/IDWriteGlyphRunAnalysis::CreateAlphaTexture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteGlyphRunAnalysis.CreateAlphaTexture
---

# IDWriteGlyphRunAnalysis::CreateAlphaTexture


## -description

 Creates an alpha texture of the specified type for glyphs within a specified bounding rectangle.

## -parameters

### -param textureType

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_texture_type">DWRITE_TEXTURE_TYPE</a></b>

A value that specifies the type of texture requested. This can be <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_texture_type">DWRITE_TEXTURE_BILEVEL_1x1</a> or <b>DWRITE_TEXTURE_CLEARTYPE_3x1</b>. If a bi-level texture is requested, the
     texture contains only bi-level glyphs. Otherwise, the texture contains only antialiased glyphs.

### -param textureBounds [in]

Type: <b>const RECT*</b>

The bounding rectangle of the texture, which can be different than
     the bounding rectangle returned by <a href="/windows/win32/api/dwrite/nf-dwrite-idwriteglyphrunanalysis-getalphatexturebounds">GetAlphaTextureBounds</a>.

### -param alphaValues [out]

Type: <b>BYTE*</b>

When this method returns, contains  the array of alpha values from the texture. The buffer allocated for this array must be at least the size of <i>bufferSize</i>.

### -param bufferSize

Type: <b>UINT32</b>

The size of the <i>alphaValues</i> array, in bytes. The minimum size depends on the dimensions of the
     rectangle and the type of texture requested.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis">IDWriteGlyphRunAnalysis</a>

