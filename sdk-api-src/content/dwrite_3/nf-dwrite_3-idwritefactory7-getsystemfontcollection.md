---
UID: NF:dwrite_3.IDWriteFactory7.GetSystemFontCollection
title: IDWriteFactory7::GetSystemFontCollection
description: Retrieves a collection of fonts, grouped into families.
helpviewer_keywords: ["IDWriteFactory7 interface [Direct Write]","GetSystemFontCollection method","IDWriteFactory7.GetSystemFontCollection","IDWriteFactory7::GetSystemFontCollection","GetSystemFontCollection","GetSystemFontCollection method [Direct Write]","GetSystemFontCollection method [Direct Write]","IDWriteFactory7 interface","directwrite.idwritefactory7_getsystemfontcollection","dwrite_3/IDWriteFactory7::GetSystemFontCollection"]
tech.root: DirectWrite
ms.date: 09/12/2019
ms.keywords: IDWriteFactory7 interface [Direct Write],GetSystemFontCollection method, IDWriteFactory7.GetSystemFontCollection, IDWriteFactory7::GetSystemFontCollection, GetSystemFontCollection, GetSystemFontCollection method [Direct Write], GetSystemFontCollection method [Direct Write],IDWriteFactory7 interface, directwrite.idwritefactory7_getsystemfontcollection, dwrite_3/IDWriteFactory7::GetSystemFontCollection
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IDWriteFactory7::GetSystemFontCollection
 - dwrite_3/IDWriteFactory7::GetSystemFontCollection
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
 - IDWriteFactory7::GetSystemFontCollection
---

## -description

Retrieves a collection of fonts, grouped into families.

## -parameters

### -param includeDownloadableFonts

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if you want to include downloadable fonts. `false` if you only want locally installed fonts.

### -param fontFamilyModel

Type: **[DWRITE_FONT_FAMILY_MODEL](./ne-dwrite_3-dwrite_font_family_model.md)**

How to group families in the collection.

### -param fontCollection [out]

Type: **[IDWriteFontCollection3](./nn-dwrite_3-idwritefontcollection3.md)\*\***

The address of a pointer to an [IDWriteFontCollection3](./nn-dwrite_3-idwritefontcollection3.md) interface. On successful completion, the function sets the pointer to a newly created font collection object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also