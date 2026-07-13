---
UID: NF:dwrite_3.IDWriteFactory5.CreateFontSetBuilder
title: IDWriteFactory5::CreateFontSetBuilder (dwrite_3.h)
description: Creates an empty font set builder to add font face references and create a custom font set. (IDWriteFactory5.CreateFontSetBuilder)
helpviewer_keywords: ["CreateFontSetBuilder","CreateFontSetBuilder method [Direct Write]","CreateFontSetBuilder method [Direct Write]","IDWriteFactory5 interface","IDWriteFactory5 interface [Direct Write]","CreateFontSetBuilder method","IDWriteFactory5.CreateFontSetBuilder","IDWriteFactory5::CreateFontSetBuilder","directwrite.idwritefactory5_createfontsetbuilder","dwrite_3/IDWriteFactory5::CreateFontSetBuilder"]
old-location: directwrite\idwritefactory5_createfontsetbuilder.htm
tech.root: DirectWrite
ms.assetid: 80E2E906-7596-4E39-808A-5CCA69376903
ms.date: 09/10/2025
ms.keywords: CreateFontSetBuilder, CreateFontSetBuilder method [Direct Write], CreateFontSetBuilder method [Direct Write],IDWriteFactory5 interface, IDWriteFactory5 interface [Direct Write],CreateFontSetBuilder method, IDWriteFactory5.CreateFontSetBuilder, IDWriteFactory5::CreateFontSetBuilder, directwrite.idwritefactory5_createfontsetbuilder, dwrite_3/IDWriteFactory5::CreateFontSetBuilder
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 15063
req.target-min-winversvr: Windows 10 Build 15063
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
 - IDWriteFactory5::CreateFontSetBuilder
 - dwrite_3/IDWriteFactory5::CreateFontSetBuilder
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
 - IDWriteFactory5.CreateFontSetBuilder
---

# IDWriteFactory5::CreateFontSetBuilder


## -description

Creates an empty font set builder to add font face references and create a custom font set.

## -parameters

### -param fontSetBuilder [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1">IDWriteFontSetBuilder1</a>**</b>

Holds the newly created font set builder object, or NULL in case of failure.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/win32/DirectWrite/custom-font-sets-win10">Custom Font Sets</a>



<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a>

