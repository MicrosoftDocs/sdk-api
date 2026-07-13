---
UID: NF:dwrite_3.IDWriteFactory6.CreateFontSetBuilder
title: IDWriteFactory6::CreateFontSetBuilder
description: Creates an empty font set builder, ready to add font instances to, and create a custom font set.
helpviewer_keywords: ["IDWriteFactory6 interface [Direct Write]","CreateFontSetBuilder method","IDWriteFactory6.CreateFontSetBuilder","IDWriteFactory6::CreateFontSetBuilder","CreateFontSetBuilder","CreateFontSetBuilder method [Direct Write]","CreateFontSetBuilder method [Direct Write]","IDWriteFactory6 interface","directwrite.idwritefactory6_createfontsetbuilder","dwrite_3/IDWriteFactory6::CreateFontSetBuilder"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteFactory6 interface [Direct Write],CreateFontSetBuilder method, IDWriteFactory6.CreateFontSetBuilder, IDWriteFactory6::CreateFontSetBuilder, CreateFontSetBuilder, CreateFontSetBuilder method [Direct Write], CreateFontSetBuilder method [Direct Write],IDWriteFactory6 interface, directwrite.idwritefactory6_createfontsetbuilder, dwrite_3/IDWriteFactory6::CreateFontSetBuilder
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 16299
req.target-min-winversvr: Windows 10 Build 16299
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
f1_keywords:
 - IDWriteFactory6::CreateFontSetBuilder
 - dwrite_3/IDWriteFactory6::CreateFontSetBuilder
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
 - IDWriteFactory6::CreateFontSetBuilder
---

## -description

Creates an empty font set builder, ready to add font instances to, and create a custom font set.

## -parameters

### -param fontSetBuilder

Type: **[IDWriteFontSetBuilder2](./nn-dwrite_3-idwritefontsetbuilder2.md)\*\***

The address of a pointer to an [IDWriteFontSetBuilder2](./nn-dwrite_3-idwritefontsetbuilder2.md) interface. On successful completion, the function sets the pointer to a newly created font set builder object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
