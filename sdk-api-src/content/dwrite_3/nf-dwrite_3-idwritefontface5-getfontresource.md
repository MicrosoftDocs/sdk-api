---
UID: NF:dwrite_3.IDWriteFontFace5.GetFontResource
title: IDWriteFontFace5::GetFontResource
description: Retrieves the underlying font resource for this font face.
helpviewer_keywords: ["IDWriteFontFace5 interface [Direct Write]","GetFontResource method","IDWriteFontFace5.GetFontResource","IDWriteFontFace5::GetFontResource","GetFontResource","GetFontResource method [Direct Write]","GetFontResource method [Direct Write]","IDWriteFontFace5 interface","directwrite.idwritefontface5_getfontresource","dwrite_3/IDWriteFontFace5::GetFontResource"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: IDWriteFontFace5 interface [Direct Write],GetFontResource method, IDWriteFontFace5.GetFontResource, IDWriteFontFace5::GetFontResource, GetFontResource, GetFontResource method [Direct Write], GetFontResource method [Direct Write],IDWriteFontFace5 interface, directwrite.idwritefontface5_getfontresource, dwrite_3/IDWriteFontFace5::GetFontResource
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
 - IDWriteFontFace5::GetFontResource
 - dwrite_3/IDWriteFontFace5::GetFontResource
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
 - IDWriteFontFace5::GetFontResource
---

## -description

Retrieves the underlying font resource for this font face. You can use that to query information about the resource, or to recreate a new font face instance with different axis values.

## -parameters

### -param fontResource [out]

Type: **[IDWriteFontResource](./nn-dwrite_3-idwritefontresource.md)\*\***

The address of a pointer to an [IDWriteFontResource](./nn-dwrite_3-idwritefontresource.md) interface. On successful completion, the function sets the pointer to a newly created font resource object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
