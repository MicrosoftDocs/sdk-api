---
UID: NF:dwrite_3.IDWriteFontSet1.CreateFontResource
title: IDWriteFontSet1::CreateFontResource
description: Creates the font resource of a single item.
helpviewer_keywords: ["IDWriteFontSet1 interface [Direct Write]","CreateFontResource method","IDWriteFontSet1.CreateFontResource","IDWriteFontSet1::CreateFontResource","CreateFontResource","CreateFontResource method [Direct Write]","CreateFontResource method [Direct Write]","IDWriteFontSet1 interface","directwrite.idwritefontset1_createfontresource","dwrite_3/IDWriteFontSet1::CreateFontResource"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet1 interface [Direct Write],CreateFontResource method, IDWriteFontSet1.CreateFontResource, IDWriteFontSet1::CreateFontResource, CreateFontResource, CreateFontResource method [Direct Write], CreateFontResource method [Direct Write],IDWriteFontSet1 interface, directwrite.idwritefontset1_createfontresource, dwrite_3/IDWriteFontSet1::CreateFontResource
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
 - IDWriteFontSet1::CreateFontResource
 - dwrite_3/IDWriteFontSet1::CreateFontResource
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
 - IDWriteFontSet1::CreateFontResource
---

## -description

Creates the font resource of a single item.

## -parameters

### -param listIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Zero-based index of the font item in the set.

### -param fontResource [out]

Type: **[IDWriteFontResource](./nn-dwrite_3-idwritefontresource.md)\*\***

The address of a pointer to an [IDWriteFontResource](./nn-dwrite_3-idwritefontresource.md) interface. On successful completion, the function sets the pointer to a newly created font resource object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|DWRITE_E_REMOTEFONT|The file is not local.|

## -remarks

## -see-also
