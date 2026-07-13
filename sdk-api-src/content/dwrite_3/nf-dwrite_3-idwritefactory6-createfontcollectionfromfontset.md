---
UID: NF:dwrite_3.IDWriteFactory6.CreateFontCollectionFromFontSet
title: IDWriteFactory6::CreateFontCollectionFromFontSet
description: From a font set, create a collection of fonts grouped into families.
helpviewer_keywords: ["IDWriteFactory6 interface [Direct Write]","CreateFontCollectionFromFontSet method","IDWriteFactory6.CreateFontCollectionFromFontSet","IDWriteFactory6::CreateFontCollectionFromFontSet","CreateFontCollectionFromFontSet","CreateFontCollectionFromFontSet method [Direct Write]","CreateFontCollectionFromFontSet method [Direct Write]","IDWriteFactory6 interface","directwrite.idwritefactory6_createfontcollectionfromfontset","dwrite_3/IDWriteFactory6::CreateFontCollectionFromFontSet"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteFactory6 interface [Direct Write],CreateFontCollectionFromFontSet method, IDWriteFactory6.CreateFontCollectionFromFontSet, IDWriteFactory6::CreateFontCollectionFromFontSet, CreateFontCollectionFromFontSet, CreateFontCollectionFromFontSet method [Direct Write], CreateFontCollectionFromFontSet method [Direct Write],IDWriteFactory6 interface, directwrite.idwritefactory6_createfontcollectionfromfontset, dwrite_3/IDWriteFactory6::CreateFontCollectionFromFontSet
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
 - IDWriteFactory6::CreateFontCollectionFromFontSet
 - dwrite_3/IDWriteFactory6::CreateFontCollectionFromFontSet
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
 - IDWriteFactory6::CreateFontCollectionFromFontSet
---

## -description

From a font set, create a collection of fonts grouped into families.

## -parameters

### -param fontSet

Type: **[IDWriteFontSet](./nn-dwrite_3-idwritefontset.md)\***

A set of fonts to use to build the collection.

### -param fontFamilyModel

Type: **[DWRITE_FONT_FAMILY_MODEL](./ne-dwrite_3-dwrite_font_family_model.md)**

How to group families in the collection.

### -param fontCollection [out]

Type: **[IDWriteFontCollection2](./nn-dwrite_3-idwritefontcollection2.md)\*\***

The address of a pointer to an [IDWriteFontCollection2](./nn-dwrite_3-idwritefontcollection2.md) interface. On successful completion, the function sets the pointer to a newly created font collection object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
