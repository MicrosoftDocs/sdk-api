---
UID: NF:dwrite_3.IDWriteFontFace3.GetFaceNames
title: IDWriteFontFace3::GetFaceNames (dwrite_3.h)
description: Creates a localized strings object that contains the face names for the font (for example, Regular or Bold), indexed by locale name.
helpviewer_keywords: ["GetFaceNames","GetFaceNames method [Direct Write]","GetFaceNames method [Direct Write]","IDWriteFontFace3 interface","IDWriteFontFace3 interface [Direct Write]","GetFaceNames method","IDWriteFontFace3.GetFaceNames","IDWriteFontFace3::GetFaceNames","directwrite.idwritefontface3_getfacenames","dwrite_3/IDWriteFontFace3::GetFaceNames"]
old-location: directwrite\idwritefontface3_getfacenames.htm
tech.root: DirectWrite
ms.assetid: 81FBE594-3429-4E61-9A83-513605879D2D
ms.date: 09/10/2025
ms.keywords: GetFaceNames, GetFaceNames method [Direct Write], GetFaceNames method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],GetFaceNames method, IDWriteFontFace3.GetFaceNames, IDWriteFontFace3::GetFaceNames, directwrite.idwritefontface3_getfacenames, dwrite_3/IDWriteFontFace3::GetFaceNames
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
 - IDWriteFontFace3::GetFaceNames
 - dwrite_3/IDWriteFontFace3::GetFaceNames
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
 - IDWriteFontFace3.GetFaceNames
---

# IDWriteFontFace3::GetFaceNames


## -description

Creates a localized strings object that contains the face names for the font (for example, Regular or Bold), indexed by locale name.

## -parameters

### -param names [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a> interface for the newly created localized strings object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>

