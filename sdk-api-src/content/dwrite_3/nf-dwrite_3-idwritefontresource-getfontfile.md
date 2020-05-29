---
UID: NF:dwrite_3.IDWriteFontResource.GetFontFile
title: IDWriteFontResource::GetFontFile
description: Retrieves the font file of the resource.
helpviewer_keywords: ["IDWriteFontResource interface [Direct Write]","GetFontFile method","IDWriteFontResource.GetFontFile","IDWriteFontResource::GetFontFile","GetFontFile","GetFontFile method [Direct Write]","GetFontFile method [Direct Write]","IDWriteFontResource interface","directwrite.idwritefontresource_getfontfile","dwrite_3/IDWriteFontResource::GetFontFile"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontResource interface [Direct Write],GetFontFile method, IDWriteFontResource.GetFontFile, IDWriteFontResource::GetFontFile, GetFontFile, GetFontFile method [Direct Write], GetFontFile method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_getfontfile, dwrite_3/IDWriteFontResource::GetFontFile
f1_keywords:
- dwrite_3/IDWriteFontResource.GetFontFile
dev_langs:
- c++
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dwrite.lib
- Dwrite.dll
api_name:
- IDWriteFontResource::GetFontFile
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the font file of the resource.

## -parameters

### -param fontFile [out]

Type: **[IDWriteFontFile](https://docs.microsoft.com/en-us/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)\*\***

The address of a pointer to an [IDWriteFontFile](https://docs.microsoft.com/en-us/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) interface. On successful completion, the function sets the pointer to the font file object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
