---
UID: NF:dwrite.IDWriteFactory.CreateFontFace
title: IDWriteFactory::CreateFontFace (dwrite.h)
description: Creates an object that represents a font face.
helpviewer_keywords: ["CreateFontFace","CreateFontFace method [Direct Write]","CreateFontFace method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateFontFace method","IDWriteFactory.CreateFontFace","IDWriteFactory::CreateFontFace","directwrite.IDWriteFactory_CreateFontFace","dwrite/IDWriteFactory::CreateFontFace"]
old-location: directwrite\IDWriteFactory_CreateFontFace.htm
tech.root: DirectWrite
ms.assetid: bb3cd53f-a2cf-472c-aee9-88ac553f0ed0
ms.date: 12/05/2018
ms.keywords: CreateFontFace, CreateFontFace method [Direct Write], CreateFontFace method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateFontFace method, IDWriteFactory.CreateFontFace, IDWriteFactory::CreateFontFace, directwrite.IDWriteFactory_CreateFontFace, dwrite/IDWriteFactory::CreateFontFace
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
 - IDWriteFactory::CreateFontFace
 - dwrite/IDWriteFactory::CreateFontFace
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
 - IDWriteFactory.CreateFontFace
---

# IDWriteFactory::CreateFontFace


## -description

 Creates an object that represents a font face.

## -parameters

### -param fontFaceType

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_face_type">DWRITE_FONT_FACE_TYPE</a></b>

A value that indicates the type of file format of the font face.

### -param numberOfFiles

Type: <b>UINT32</b>

The number of font files, in element count, required to represent the font face.

### -param fontFiles [in]

Type: <b>const <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>*</b>

A font file object representing the font face.  Because <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a> maintains its own references
     to the input font file objects, you may release them after this call.

### -param faceIndex

Type: <b>UINT32</b>

The zero-based index of a font face, in cases when the font files contain a collection of font faces.
     If the font files contain a single face, this value should be zero.

### -param fontFaceSimulationFlags

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations">DWRITE_FONT_SIMULATIONS</a></b>

A value that indicates which, if any, font face simulation flags for algorithmic means of making text bold or italic are applied to the current font face.

### -param fontFace [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>**</b>

When this method returns, contains an address of a pointer to the newly created font face object, or <b>NULL</b> in case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

