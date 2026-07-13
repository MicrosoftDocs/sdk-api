---
UID: NF:dwrite_3.IDWriteFont3.CreateFontFace
title: IDWriteFont3::CreateFontFace (dwrite_3.h)
description: Creates a font face object for the font. (IDWriteFont3.CreateFontFace)
helpviewer_keywords: ["CreateFontFace","CreateFontFace method [Direct Write]","CreateFontFace method [Direct Write]","IDWriteFont3 interface","IDWriteFont3 interface [Direct Write]","CreateFontFace method","IDWriteFont3.CreateFontFace","IDWriteFont3::CreateFontFace","directwrite.idwritefont3_createfontface","dwrite_3/IDWriteFont3::CreateFontFace"]
old-location: directwrite\idwritefont3_createfontface.htm
tech.root: DirectWrite
ms.assetid: 451B8B33-4EA5-4BE3-A126-AAC01D35CE35
ms.date: 09/10/2025
ms.keywords: CreateFontFace, CreateFontFace method [Direct Write], CreateFontFace method [Direct Write],IDWriteFont3 interface, IDWriteFont3 interface [Direct Write],CreateFontFace method, IDWriteFont3.CreateFontFace, IDWriteFont3::CreateFontFace, directwrite.idwritefont3_createfontface, dwrite_3/IDWriteFont3::CreateFontFace
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
 - IDWriteFont3::CreateFontFace
 - dwrite_3/IDWriteFont3::CreateFontFace
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
 - IDWriteFont3.CreateFontFace
---

# IDWriteFont3::CreateFontFace


## -description

Creates a font face object for the font.

## -parameters

### -param fontFace [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a> interface for the newly created font face object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.



This method returns <b>DWRITE_E_REMOTEFONT</b> if it could not construct a remote font.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3">IDWriteFont3</a>

