---
UID: NF:dwrite_3.IDWriteFontFaceReference.CreateFontFace
title: IDWriteFontFaceReference::CreateFontFace (dwrite_3.h)
description: Creates a font face from the reference for use with layout, shaping, or rendering.
helpviewer_keywords: ["CreateFontFace","CreateFontFace method [Direct Write]","CreateFontFace method [Direct Write]","IDWriteFontFaceReference interface","IDWriteFontFaceReference interface [Direct Write]","CreateFontFace method","IDWriteFontFaceReference.CreateFontFace","IDWriteFontFaceReference::CreateFontFace","directwrite.idwritefontfacereference_createfontface","dwrite_3/IDWriteFontFaceReference::CreateFontFace"]
old-location: directwrite\idwritefontfacereference_createfontface.htm
tech.root: DirectWrite
ms.assetid: f9bc5933-c766-5b30-e2cf-b276a80aecda
ms.date: 09/10/2025
ms.keywords: CreateFontFace, CreateFontFace method [Direct Write], CreateFontFace method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],CreateFontFace method, IDWriteFontFaceReference.CreateFontFace, IDWriteFontFaceReference::CreateFontFace, directwrite.idwritefontfacereference_createfontface, dwrite_3/IDWriteFontFaceReference::CreateFontFace
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
 - IDWriteFontFaceReference::CreateFontFace
 - dwrite_3/IDWriteFontFaceReference::CreateFontFace
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
 - IDWriteFontFaceReference.CreateFontFace
---

# IDWriteFontFaceReference::CreateFontFace


## -description

Creates a font face from the reference for use with layout, shaping, or rendering.

## -parameters

### -param fontFace [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>**</b>

Newly created font face object, or nullptr in the case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function can fail with DWRITE_E_REMOTEFONT if the font is not local.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>

