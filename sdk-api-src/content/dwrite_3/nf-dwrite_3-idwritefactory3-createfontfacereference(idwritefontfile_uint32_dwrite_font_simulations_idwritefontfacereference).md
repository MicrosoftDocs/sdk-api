---
UID: NF:dwrite_3.IDWriteFactory3.CreateFontFaceReference(IDWriteFontFile,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference)
title: IDWriteFactory3::CreateFontFaceReference(IDWriteFontFile,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference) (dwrite_3.h)
description: Creates a reference to a font given a full path. (overload 1/2)
helpviewer_keywords: ["CreateFontFaceReference","CreateFontFaceReference method [Direct Write]","CreateFontFaceReference method [Direct Write]","IDWriteFactory3 interface","IDWriteFactory3 interface [Direct Write]","CreateFontFaceReference method","IDWriteFactory3.CreateFontFaceReference","IDWriteFactory3.CreateFontFaceReference(IDWriteFontFile","UINT32","DWRITE_FONT_SIMULATIONS","IDWriteFontFaceReference)","IDWriteFactory3::CreateFontFaceReference","IDWriteFactory3::CreateFontFaceReference(IDWriteFontFile","UINT32","DWRITE_FONT_SIMULATIONS","IDWriteFontFaceReference)","directwrite.idwritefactory3_createfontfacereference","dwrite_3/IDWriteFactory3::CreateFontFaceReference"]
old-location: directwrite\idwritefactory3_createfontfacereference.htm
tech.root: DirectWrite
ms.assetid: 3ae2150b-af56-65f5-fe38-7ecea16cf0b8
ms.date: 09/10/2025
ms.keywords: CreateFontFaceReference, CreateFontFaceReference method [Direct Write], CreateFontFaceReference method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],CreateFontFaceReference method, IDWriteFactory3.CreateFontFaceReference, IDWriteFactory3.CreateFontFaceReference(IDWriteFontFile,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference), IDWriteFactory3::CreateFontFaceReference, IDWriteFactory3::CreateFontFaceReference(IDWriteFontFile,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference), directwrite.idwritefactory3_createfontfacereference, dwrite_3/IDWriteFactory3::CreateFontFaceReference
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFactory3::CreateFontFaceReference
 - dwrite_3/IDWriteFactory3::CreateFontFaceReference
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
 - IDWriteFactory3.CreateFontFaceReference
---

# IDWriteFactory3::CreateFontFaceReference(IDWriteFontFile,UINT32,DWRITE_FONT_SIMULATIONS,IDWriteFontFaceReference)


## -description

Creates a reference to a font given an **IDWriteFontFile**.

## -parameters

### -param fontFile

An **IDWriteFontFile** representing the font face.

### -param faceIndex

Type: <b>UINT32</b>

The zero based index of a font face in cases when the font files contain a collection of font faces.      
          If the font files contain a single face, this value should be zero.

### -param fontSimulations

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations">DWRITE_FONT_SIMULATIONS</a></b>

Font face simulation flags for algorithmic emboldening and italicization.

### -param fontFaceReference [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>**</b>

Contains newly created font face reference object, or nullptr in case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a>

