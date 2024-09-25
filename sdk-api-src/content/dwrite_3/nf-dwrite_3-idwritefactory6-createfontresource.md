---
UID: NF:dwrite_3.IDWriteFactory6.CreateFontResource
title: IDWriteFactory6::CreateFontResource
description: Creates a font resource, given a font file and a face index.
helpviewer_keywords: ["IDWriteFactory6 interface [Direct Write]","CreateFontResource method","IDWriteFactory6.CreateFontResource","IDWriteFactory6::CreateFontResource","CreateFontResource","CreateFontResource method [Direct Write]","CreateFontResource method [Direct Write]","IDWriteFactory6 interface","directwrite.idwritefactory6_createfontresource","dwrite_3/IDWriteFactory6::CreateFontResource"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: IDWriteFactory6 interface [Direct Write],CreateFontResource method, IDWriteFactory6.CreateFontResource, IDWriteFactory6::CreateFontResource, CreateFontResource, CreateFontResource method [Direct Write], CreateFontResource method [Direct Write],IDWriteFactory6 interface, directwrite.idwritefactory6_createfontresource, dwrite_3/IDWriteFactory6::CreateFontResource
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
 - IDWriteFactory6::CreateFontResource
 - dwrite_3/IDWriteFactory6::CreateFontResource
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
 - IDWriteFactory6::CreateFontResource
---

## -description

Creates a font resource, given a font file and a face index.

## -parameters

### -param fontFile

Type: **[IDWriteFontFile](../dwrite/nn-dwrite-idwritefontfile.md)\***

A user-provided font file representing the font face.

### -param faceIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The zero-based index of a font face in cases when the font file contains a collection of font faces. If the font file contains a single face, then set this value to zero.

### -param fontResource

Type: **[IDWriteFontResource](./nn-dwrite_3-idwritefontresource.md)\*\***

The address of a pointer to an [IDWriteFontResource](./nn-dwrite_3-idwritefontresource.md) interface. On successful completion, the function sets the pointer to a newly created font resource object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
