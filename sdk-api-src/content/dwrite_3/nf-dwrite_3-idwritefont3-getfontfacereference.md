---
UID: NF:dwrite_3.IDWriteFont3.GetFontFaceReference
title: IDWriteFont3::GetFontFaceReference (dwrite_3.h)
description: Gets a font face reference that identifies this font. (IDWriteFont3.GetFontFaceReference)
helpviewer_keywords: ["GetFontFaceReference","GetFontFaceReference method [Direct Write]","GetFontFaceReference method [Direct Write]","IDWriteFont3 interface","IDWriteFont3 interface [Direct Write]","GetFontFaceReference method","IDWriteFont3.GetFontFaceReference","IDWriteFont3::GetFontFaceReference","directwrite.idwritefont3_getfontfacereference","dwrite_3/IDWriteFont3::GetFontFaceReference"]
old-location: directwrite\idwritefont3_getfontfacereference.htm
tech.root: DirectWrite
ms.assetid: 8939ADA0-B2D9-4489-B9AC-EA37776F6340
ms.date: 09/10/2025
ms.keywords: GetFontFaceReference, GetFontFaceReference method [Direct Write], GetFontFaceReference method [Direct Write],IDWriteFont3 interface, IDWriteFont3 interface [Direct Write],GetFontFaceReference method, IDWriteFont3.GetFontFaceReference, IDWriteFont3::GetFontFaceReference, directwrite.idwritefont3_getfontfacereference, dwrite_3/IDWriteFont3::GetFontFaceReference
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
 - IDWriteFont3::GetFontFaceReference
 - dwrite_3/IDWriteFont3::GetFontFaceReference
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
 - IDWriteFont3.GetFontFaceReference
---

# IDWriteFont3::GetFontFaceReference


## -description

Gets a font face reference that identifies this font.

## -parameters

### -param fontFaceReference [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a> interface for the newly created font face reference object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3">IDWriteFont3</a>

