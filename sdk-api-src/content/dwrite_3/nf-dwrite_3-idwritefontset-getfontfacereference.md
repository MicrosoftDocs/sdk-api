---
UID: NF:dwrite_3.IDWriteFontSet.GetFontFaceReference
title: IDWriteFontSet::GetFontFaceReference (dwrite_3.h)
description: Gets a reference to the font at the specified index, which may be local or remote.
helpviewer_keywords: ["GetFontFaceReference","GetFontFaceReference method [Direct Write]","GetFontFaceReference method [Direct Write]","IDWriteFontSet interface","IDWriteFontSet interface [Direct Write]","GetFontFaceReference method","IDWriteFontSet.GetFontFaceReference","IDWriteFontSet::GetFontFaceReference","directwrite.idwritefontset_getfontfacereference","dwrite_3/IDWriteFontSet::GetFontFaceReference"]
old-location: directwrite\idwritefontset_getfontfacereference.htm
tech.root: DirectWrite
ms.assetid: 8cbc1275-29d5-917d-6938-8fb35e5054fb
ms.date: 09/10/2025
ms.keywords: GetFontFaceReference, GetFontFaceReference method [Direct Write], GetFontFaceReference method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],GetFontFaceReference method, IDWriteFontSet.GetFontFaceReference, IDWriteFontSet::GetFontFaceReference, directwrite.idwritefontset_getfontfacereference, dwrite_3/IDWriteFontSet::GetFontFaceReference
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
 - IDWriteFontSet::GetFontFaceReference
 - dwrite_3/IDWriteFontSet::GetFontFaceReference
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
 - IDWriteFontSet.GetFontFaceReference
---

# IDWriteFontSet::GetFontFaceReference


## -description

Gets a reference to the font at the specified index, which may be local or remote.

## -parameters

### -param listIndex

Type: <b>UINT32</b>

Zero-based index of the font.

### -param fontFaceReference [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference">IDWriteFontFaceReference</a>**</b>

Receives a pointer the font face reference object, or nullptr on failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>

